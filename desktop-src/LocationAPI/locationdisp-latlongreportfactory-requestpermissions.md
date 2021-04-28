---
description: Método LocationDisp. LatLongReportFactory. RequestPermissions – abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Método LocationDisp. LatLongReportFactory. RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b2d21a032a2e4c08c6f80e4f0ae79349a49ce21
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088924"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="b6c76-103">Método LocationDisp. LatLongReportFactory. RequestPermissions</span><span class="sxs-lookup"><span data-stu-id="b6c76-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="b6c76-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6c76-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6c76-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="b6c76-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b6c76-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6c76-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="b6c76-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="b6c76-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="b6c76-108">Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.</span><span class="sxs-lookup"><span data-stu-id="b6c76-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c76-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6c76-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="b6c76-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6c76-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c76-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="b6c76-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b6c76-112">Esse parâmetro não é usado e deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b6c76-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c76-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b6c76-113">Return value</span></span>

<span data-ttu-id="b6c76-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b6c76-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c76-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c76-115">Remarks</span></span>

<span data-ttu-id="b6c76-116">A chamada é síncrona e o chamador aguarda a caixa de diálogo ser fechada.</span><span class="sxs-lookup"><span data-stu-id="b6c76-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="b6c76-117">Se um aplicativo executado no modo protegido, como um BHO (objeto auxiliar de navegador) para o Internet Explorer, chamar **RequestPermissions** e o usuário escolher a opção **não habilitar este sensor de local** na caixa de diálogo, o provedor de localização não será habilitado, mas o Windows exibirá a caixa de diálogo novamente se **RequestPermissions** for chamado novamente pelo mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="b6c76-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="b6c76-118">Os aplicativos executados no modo protegido podem optar por não chamar **RequestPermissions** na inicialização para que o usuário não veja uma caixa de diálogo possivelmente indesejado sempre que o aplicativo for iniciado.</span><span class="sxs-lookup"><span data-stu-id="b6c76-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b6c76-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b6c76-119">Examples</span></span>

<span data-ttu-id="b6c76-120">Para obter um exemplo de como usar esse método, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="b6c76-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c76-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6c76-121">Requirements</span></span>



| <span data-ttu-id="b6c76-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c76-122">Requirement</span></span> | <span data-ttu-id="b6c76-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b6c76-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="b6c76-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c76-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c76-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6c76-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6c76-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c76-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c76-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b6c76-127">None supported</span></span><br/>                  |



 

