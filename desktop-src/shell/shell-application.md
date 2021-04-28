---
description: Propriedade Shell. Application – contém o objeto Application do objeto.
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
ms.openlocfilehash: 5a90b3953ed54b8a3652d6c9c26533d433ffb600
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083854"
---
# <a name="shellapplication-property"></a><span data-ttu-id="68305-103">Propriedade Shell. Application</span><span class="sxs-lookup"><span data-stu-id="68305-103">Shell.Application property</span></span>

<span data-ttu-id="68305-104">Contém o objeto de aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="68305-104">Contains the object's Application object.</span></span>

<span data-ttu-id="68305-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="68305-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68305-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68305-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="68305-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="68305-107">Property value</span></span>

<span data-ttu-id="68305-108">Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68305-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="68305-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="68305-109">Remarks</span></span>

<span data-ttu-id="68305-110">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="68305-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="68305-111">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="68305-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="68305-112">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="68305-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="68305-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68305-113">Requirements</span></span>



| <span data-ttu-id="68305-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="68305-114">Requirement</span></span> | <span data-ttu-id="68305-115">Valor</span><span class="sxs-lookup"><span data-stu-id="68305-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68305-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68305-116">Minimum supported client</span></span><br/> | <span data-ttu-id="68305-117">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="68305-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="68305-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68305-118">Minimum supported server</span></span><br/> | <span data-ttu-id="68305-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68305-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="68305-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="68305-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="68305-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68305-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="68305-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="68305-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68305-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68305-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="68305-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68305-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68305-125"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="68305-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
