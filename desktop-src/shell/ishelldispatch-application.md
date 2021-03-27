---
description: Contém um objeto que representa um aplicativo.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Propriedade IShellDispatch. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502090"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="b674d-103">Propriedade IShellDispatch. Application</span><span class="sxs-lookup"><span data-stu-id="b674d-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="b674d-104">Contém um objeto que representa um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b674d-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="b674d-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b674d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b674d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b674d-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="b674d-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b674d-107">Property value</span></span>

<span data-ttu-id="b674d-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b674d-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b674d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b674d-109">Remarks</span></span>

<span data-ttu-id="b674d-110">Essa propriedade é implementada e acessada por meio da propriedade [**shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="b674d-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="b674d-111">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="b674d-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="b674d-112">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="b674d-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="b674d-113">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b674d-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b674d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b674d-114">Requirements</span></span>



| <span data-ttu-id="b674d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b674d-115">Requirement</span></span> | <span data-ttu-id="b674d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b674d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b674d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b674d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b674d-118">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b674d-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b674d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b674d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b674d-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b674d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b674d-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b674d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b674d-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b674d-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b674d-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="b674d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b674d-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b674d-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b674d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b674d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b674d-126"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b674d-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
