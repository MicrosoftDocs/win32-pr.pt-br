---
description: Contém o objeto de aplicativo do objeto.
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Propriedade ShellFolderView. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ba57c407183179f580b5b616ad039c22e6fea66c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968120"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="032cc-103">Propriedade ShellFolderView. Application</span><span class="sxs-lookup"><span data-stu-id="032cc-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="032cc-104">Contém o objeto de aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="032cc-104">Contains the object's Application object.</span></span>

<span data-ttu-id="032cc-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="032cc-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="032cc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="032cc-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="032cc-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="032cc-107">Property value</span></span>

<span data-ttu-id="032cc-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="032cc-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="032cc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="032cc-109">Remarks</span></span>

<span data-ttu-id="032cc-110">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="032cc-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="032cc-111">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="032cc-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="032cc-112">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="032cc-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="032cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032cc-113">Requirements</span></span>



| <span data-ttu-id="032cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="032cc-114">Requirement</span></span> | <span data-ttu-id="032cc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="032cc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032cc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="032cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="032cc-117">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="032cc-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="032cc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="032cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="032cc-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="032cc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="032cc-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="032cc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="032cc-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="032cc-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="032cc-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="032cc-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="032cc-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="032cc-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="032cc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="032cc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032cc-125"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="032cc-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
