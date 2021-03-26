---
description: Contém o objeto de aplicativo da pasta.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propriedade Folder. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457204"
---
# <a name="folderapplication-property"></a><span data-ttu-id="2778c-103">Propriedade Folder. Application</span><span class="sxs-lookup"><span data-stu-id="2778c-103">Folder.Application property</span></span>

<span data-ttu-id="2778c-104">Contém o objeto de aplicativo da pasta.</span><span class="sxs-lookup"><span data-stu-id="2778c-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="2778c-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2778c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2778c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2778c-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="2778c-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2778c-107">Property value</span></span>

<span data-ttu-id="2778c-108">Uma referência de objeto para o objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2778c-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2778c-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2778c-109">Remarks</span></span>

<span data-ttu-id="2778c-110">A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível.</span><span class="sxs-lookup"><span data-stu-id="2778c-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="2778c-111">Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="2778c-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="2778c-112">Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2778c-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="2778c-113">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="2778c-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="2778c-114">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="2778c-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="2778c-115">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="2778c-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2778c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2778c-116">Requirements</span></span>



| <span data-ttu-id="2778c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2778c-117">Requirement</span></span> | <span data-ttu-id="2778c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2778c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2778c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2778c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2778c-120">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2778c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="2778c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2778c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2778c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2778c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2778c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2778c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2778c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2778c-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2778c-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="2778c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2778c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2778c-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




