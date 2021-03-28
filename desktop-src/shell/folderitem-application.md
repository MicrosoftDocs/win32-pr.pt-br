---
description: Contém o objeto de aplicativo do item de pasta.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Propriedade FolderItem. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 72816ed0c426f6ff3fa92c30a1ec31757c0a02fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501159"
---
# <a name="folderitemapplication-property"></a><span data-ttu-id="a0984-103">Propriedade FolderItem. Application</span><span class="sxs-lookup"><span data-stu-id="a0984-103">FolderItem.Application property</span></span>

<span data-ttu-id="a0984-104">Contém o objeto de **aplicativo** do item de pasta.</span><span class="sxs-lookup"><span data-stu-id="a0984-104">Contains the **Application** object of the folder item.</span></span>

<span data-ttu-id="a0984-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a0984-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0984-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0984-106">Syntax</span></span>


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a><span data-ttu-id="a0984-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a0984-107">Property value</span></span>

<span data-ttu-id="a0984-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de **aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="a0984-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the **Application** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0984-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0984-109">Remarks</span></span>

<span data-ttu-id="a0984-110">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="a0984-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="a0984-111">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="a0984-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="a0984-112">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a0984-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0984-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0984-113">Requirements</span></span>



| <span data-ttu-id="a0984-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0984-114">Requirement</span></span> | <span data-ttu-id="a0984-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a0984-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0984-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0984-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a0984-117">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0984-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0984-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0984-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a0984-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a0984-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0984-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a0984-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0984-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0984-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a0984-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="a0984-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0984-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0984-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a0984-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a0984-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0984-125"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a0984-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
