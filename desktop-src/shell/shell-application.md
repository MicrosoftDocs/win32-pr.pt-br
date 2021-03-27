---
description: Contém o objeto de aplicativo do objeto.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Propriedade Shell. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9f9bd7fa28d2b277adfd8038c10c97efe16f51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837224"
---
# <a name="shellapplication-property"></a><span data-ttu-id="47c34-103">Propriedade Shell. Application</span><span class="sxs-lookup"><span data-stu-id="47c34-103">Shell.Application property</span></span>

<span data-ttu-id="47c34-104">Contém o objeto de aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="47c34-104">Contains the object's Application object.</span></span>

<span data-ttu-id="47c34-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="47c34-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c34-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47c34-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="47c34-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="47c34-107">Property value</span></span>

<span data-ttu-id="47c34-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="47c34-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c34-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="47c34-109">Remarks</span></span>

<span data-ttu-id="47c34-110">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="47c34-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="47c34-111">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="47c34-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="47c34-112">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="47c34-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="47c34-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47c34-113">Requirements</span></span>



| <span data-ttu-id="47c34-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="47c34-114">Requirement</span></span> | <span data-ttu-id="47c34-115">Valor</span><span class="sxs-lookup"><span data-stu-id="47c34-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c34-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c34-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47c34-117">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="47c34-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="47c34-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47c34-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47c34-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="47c34-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="47c34-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="47c34-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47c34-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c34-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="47c34-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="47c34-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47c34-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47c34-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="47c34-124">DLL</span><span class="sxs-lookup"><span data-stu-id="47c34-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c34-125"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="47c34-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
