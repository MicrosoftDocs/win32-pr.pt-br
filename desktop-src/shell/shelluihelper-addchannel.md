---
description: Adiciona um novo canal à lista de canais no menu Favoritos do Windows Internet Explorer e à barra de canais na área de trabalho.
title: Método ShellUIHelper. addchannel (textdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: 93c62abd8f788f950e36bcfc5fa10f7c991a6410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989098"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="4f8cd-103">Método ShellUIHelper. addchannel</span><span class="sxs-lookup"><span data-stu-id="4f8cd-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="4f8cd-104">Adiciona um novo canal à lista de canais no menu **favoritos** do Windows Internet Explorer e à barra de **canais** na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="4f8cd-105">Não há mais suporte para esse método no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="4f8cd-106">Nesse sistema operacional, ele retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4f8cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f8cd-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="4f8cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f8cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8cd-109">*sUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f8cd-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8cd-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4f8cd-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4f8cd-111">Um valor de **cadeia de caracteres** que especifica a URL do arquivo CDF.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="4f8cd-112">Os links no arquivo CDF devem usar protocolos HTTP, HTTPS ou FTP.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="4f8cd-113">Se o arquivo CDF contiver qualquer outro protocolo, a adição do canal falhará e nenhuma caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4f8cd-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f8cd-114">Examples</span></span>

<span data-ttu-id="4f8cd-115">O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4f8cd-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="4f8cd-116">JScript</span><span class="sxs-lookup"><span data-stu-id="4f8cd-116">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="4f8cd-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4f8cd-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4f8cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f8cd-118">Requirements</span></span>



| <span data-ttu-id="4f8cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8cd-119">Requirement</span></span> | <span data-ttu-id="4f8cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4f8cd-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8cd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f8cd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8cd-122">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f8cd-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4f8cd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f8cd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8cd-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4f8cd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f8cd-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4f8cd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f8cd-126"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f8cd-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="4f8cd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4f8cd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f8cd-128"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4f8cd-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
