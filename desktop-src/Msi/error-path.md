---
description: No Windows Installer versões 1,0 e 1,1, a propriedade Path é sempre a cadeia de caracteres vazia. Versões futuras podem usar esse valor para retornar o caminho para o arquivo ou diretório que não pôde ser criado.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Erro. propriedade Path (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758625"
---
# <a name="errorpath-property"></a><span data-ttu-id="ead2d-104">Propriedade Error. Path</span><span class="sxs-lookup"><span data-stu-id="ead2d-104">Error.Path property</span></span>

<span data-ttu-id="ead2d-105">No Windows Installer versões 1,0 e 1,1, a propriedade Path é sempre a cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ead2d-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="ead2d-106">Versões futuras podem usar esse valor para retornar o caminho para o arquivo ou diretório que não pôde ser criado.</span><span class="sxs-lookup"><span data-stu-id="ead2d-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="ead2d-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ead2d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead2d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ead2d-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="ead2d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ead2d-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="ead2d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ead2d-110">Remarks</span></span>

<span data-ttu-id="ead2d-111">Esse valor só é válido para erros do tipo msmErrorFileCreate ou msmErrorDirCreate.</span><span class="sxs-lookup"><span data-stu-id="ead2d-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="ead2d-112">Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ead2d-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="ead2d-113">C++</span><span class="sxs-lookup"><span data-stu-id="ead2d-113">C++</span></span>

<span data-ttu-id="ead2d-114">Consulte a função [**obter \_ caminho**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) .</span><span class="sxs-lookup"><span data-stu-id="ead2d-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead2d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead2d-115">Requirements</span></span>



| <span data-ttu-id="ead2d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead2d-116">Requirement</span></span> | <span data-ttu-id="ead2d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ead2d-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ead2d-118">Versão</span><span class="sxs-lookup"><span data-stu-id="ead2d-118">Version</span></span><br/> | <span data-ttu-id="ead2d-119">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ead2d-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="ead2d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ead2d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ead2d-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead2d-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="ead2d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ead2d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="ead2d-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead2d-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

