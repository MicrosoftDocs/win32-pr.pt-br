---
description: O método SourceListAddSource adiciona uma fonte de rede ou URL. Aceita SourcePath, tipo e índice como parâmetros. Esse método chama MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Método patch. SourceListAddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752445"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="0fd8a-105">Método patch. SourceListAddSource</span><span class="sxs-lookup"><span data-stu-id="0fd8a-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="0fd8a-106">O método **SourceListAddSource** adiciona uma fonte de rede ou URL.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="0fd8a-107">Aceita *SourcePath*, *tipo* e *índice* como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="0fd8a-108">Esse método chama [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd8a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fd8a-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="0fd8a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fd8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd8a-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="0fd8a-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd8a-112">Tipo de fonte a ser adicionada: MSISOURCETYPE \_ rede ou URL de MSISOURCETYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="0fd8a-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="0fd8a-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="0fd8a-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd8a-114">Caminho para a origem a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="0fd8a-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="0fd8a-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="0fd8a-116">Se **SourceListAddSource** for chamado com uma nova fonte e um novo *índice* definido como 0, o instalador adicionará a origem ao final da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="0fd8a-117">Se essa função for chamada com uma fonte já existente na lista de origem e o *índice* estiver definido como 0, o instalador manterá o índice existente da origem.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="0fd8a-118">Se a função for chamada com uma origem existente na lista de origem e o *índice* for definido como um valor diferente de zero, a origem será removida de seu local atual na lista e inserida na posição especificada pelo *índice*, antes de qualquer fonte que já exista nessa posição.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="0fd8a-119">Se a função for chamada com uma nova origem e um *índice* for definido como um valor diferente de zero, a origem será inserida na posição especificada pelo *índice*, antes de qualquer fonte que já exista nessa posição.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="0fd8a-120">O valor de índice para todas as fontes na lista após o índice especificado pelo *índice* é atualizado para garantir que os valores de índice exclusivos e a ordem preexistente permaneçam inalterados.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="0fd8a-121">Se o *índice* for maior que o número de fontes na lista, a origem será colocada no final da lista com um valor de índice maior do que qualquer origem existente.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd8a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fd8a-122">Return value</span></span>

<span data-ttu-id="0fd8a-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd8a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fd8a-124">Requirements</span></span>



| <span data-ttu-id="0fd8a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd8a-125">Requirement</span></span> | <span data-ttu-id="0fd8a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0fd8a-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd8a-127">Versão</span><span class="sxs-lookup"><span data-stu-id="0fd8a-127">Version</span></span><br/> | <span data-ttu-id="0fd8a-128">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0fd8a-129">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0fd8a-130">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0fd8a-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0fd8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd8a-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="0fd8a-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8a-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0fd8a-133">IID</span><span class="sxs-lookup"><span data-stu-id="0fd8a-133">IID</span></span><br/>     | <span data-ttu-id="0fd8a-134">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0fd8a-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0fd8a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fd8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd8a-136">**Patch**</span><span class="sxs-lookup"><span data-stu-id="0fd8a-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0fd8a-137">**MsiSourceListAddSourceEx**</span><span class="sxs-lookup"><span data-stu-id="0fd8a-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="0fd8a-138">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0fd8a-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




