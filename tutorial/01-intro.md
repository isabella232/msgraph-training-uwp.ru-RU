<!-- markdownlint-disable MD002 MD041 -->

<span data-ttu-id="c1d39-101">В этом руководстве рассказывается, как создать приложение для универсальной платформы Windows (UWP), которое использует API Microsoft Graph для получения сведений о календаре для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1d39-101">This tutorial teaches you how to build a Universal Windows Platform (UWP) app that uses the Microsoft Graph API to retrieve calendar information for a user.</span></span>

> [!TIP]
> <span data-ttu-id="c1d39-102">Если вы предпочитаете просто скачать заполненный учебник, вы можете скачать или клонировать [репозиторий GitHub](https://github.com/microsoftgraph/msgraph-training-uwp).</span><span class="sxs-lookup"><span data-stu-id="c1d39-102">If you prefer to just download the completed tutorial, you can download or clone the [GitHub repository](https://github.com/microsoftgraph/msgraph-training-uwp).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1d39-103">Предварительные требования</span><span class="sxs-lookup"><span data-stu-id="c1d39-103">Prerequisites</span></span>

<span data-ttu-id="c1d39-104">Прежде чем приступить к работе с этим руководством, на компьютере под управлением Windows 10 с [включенным режимом разработчика](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development)должен быть установлен [Visual Studio](https://visualstudio.microsoft.com/vs/) .</span><span class="sxs-lookup"><span data-stu-id="c1d39-104">Before you start this tutorial, you should have [Visual Studio](https://visualstudio.microsoft.com/vs/) installed on a computer running Windows 10 with [Developer mode turned on](https://docs.microsoft.com/windows/uwp/get-started/enable-your-device-for-development).</span></span> <span data-ttu-id="c1d39-105">Если у вас нет Visual Studio, посетите предыдущую ссылку для получения вариантов загрузки.</span><span class="sxs-lookup"><span data-stu-id="c1d39-105">If you do not have Visual Studio, visit the previous link for download options.</span></span>

<span data-ttu-id="c1d39-106">Кроме того, у вас также должна быть личная учетная запись Майкрософт с почтовым ящиком на Outlook.com или рабочей или учебной учетной записью Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c1d39-106">You should also have either a personal Microsoft account with a mailbox on Outlook.com, or a Microsoft work or school account.</span></span> <span data-ttu-id="c1d39-107">Если у вас нет учетной записи Майкрософт, у вас есть несколько вариантов для получения бесплатной учетной записи:</span><span class="sxs-lookup"><span data-stu-id="c1d39-107">If you don't have a Microsoft account, there are a couple of options to get a free account:</span></span>

- <span data-ttu-id="c1d39-108">Вы можете [зарегистрироваться для создания новой личной учетной записи Майкрософт](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span><span class="sxs-lookup"><span data-stu-id="c1d39-108">You can [sign up for a new personal Microsoft account](https://signup.live.com/signup?wa=wsignin1.0&rpsnv=12&ct=1454618383&rver=6.4.6456.0&wp=MBI_SSL_SHARED&wreply=https://mail.live.com/default.aspx&id=64855&cbcxt=mai&bk=1454618383&uiflavor=web&uaid=b213a65b4fdc484382b6622b3ecaa547&mkt=E-US&lc=1033&lic=1).</span></span>
- <span data-ttu-id="c1d39-109">Вы можете [зарегистрироваться в программе для разработчиков office 365](https://developer.microsoft.com/office/dev-program) , чтобы получить бесплатную подписку на Office 365.</span><span class="sxs-lookup"><span data-stu-id="c1d39-109">You can [sign up for the Office 365 Developer Program](https://developer.microsoft.com/office/dev-program) to get a free Office 365 subscription.</span></span>

> [!NOTE]
> <span data-ttu-id="c1d39-110">Это руководство было написано с помощью Visual Studio 2019 версии 16.5.0.</span><span class="sxs-lookup"><span data-stu-id="c1d39-110">This tutorial was written with Visual Studio 2019 version 16.5.0.</span></span> <span data-ttu-id="c1d39-111">Действия, описанные в этом руководстве, могут работать с другими версиями, но не тестировались.</span><span class="sxs-lookup"><span data-stu-id="c1d39-111">The steps in this guide may work with other versions, but that has not been tested.</span></span>

## <a name="watch-the-tutorial"></a><span data-ttu-id="c1d39-112">Просмотр руководства</span><span class="sxs-lookup"><span data-stu-id="c1d39-112">Watch the tutorial</span></span>

<span data-ttu-id="c1d39-113">Этот модуль записан и доступен в канале разработки Office на YouTube.</span><span class="sxs-lookup"><span data-stu-id="c1d39-113">This module has been recorded and is available in the Office Development YouTube channel.</span></span>

<!-- markdownlint-disable MD033 MD034 -->
<br/>

> [!VIDEO https://www.youtube-nocookie.com/embed/oBYCBxkWMRA]
<!-- markdownlint-enable MD033 MD034 -->

## <a name="feedback"></a><span data-ttu-id="c1d39-114">Отзывы</span><span class="sxs-lookup"><span data-stu-id="c1d39-114">Feedback</span></span>

<span data-ttu-id="c1d39-115">Сообщите о нем в [репозиторий GitHub](https://github.com/microsoftgraph/msgraph-training-uwp).</span><span class="sxs-lookup"><span data-stu-id="c1d39-115">Please provide any feedback on this tutorial in the [GitHub repository](https://github.com/microsoftgraph/msgraph-training-uwp).</span></span>
