---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: O método ConfigureFilterUsingProfileGuid configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado. (Preterido.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfileGuid
- Método ConfigureFilterUsingProfileGuid Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499123"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="d820b-107">Método IConfigAsfWriter:: ConfigureFilterUsingProfileGuid</span><span class="sxs-lookup"><span data-stu-id="d820b-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="d820b-108">O método **ConfigureFilterUsingProfileGuid** configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado.</span><span class="sxs-lookup"><span data-stu-id="d820b-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="d820b-109">(Preterido.)</span><span class="sxs-lookup"><span data-stu-id="d820b-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="d820b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d820b-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="d820b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d820b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d820b-112">*guidProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d820b-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d820b-113">**GUID** que identifica um perfil conforme definido no arquivo de cabeçalho do SDK do Windows Media Format Wmsysprf. h.</span><span class="sxs-lookup"><span data-stu-id="d820b-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d820b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d820b-114">Return value</span></span>

<span data-ttu-id="d820b-115">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="d820b-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d820b-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d820b-116">Return code</span></span>                                                                                         | <span data-ttu-id="d820b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d820b-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d820b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d820b-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="d820b-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d820b-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="d820b-120"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="d820b-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="d820b-121">O perfil não é válido.</span><span class="sxs-lookup"><span data-stu-id="d820b-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="d820b-122"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d820b-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="d820b-123">O grafo de filtro é interrompido.</span><span class="sxs-lookup"><span data-stu-id="d820b-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d820b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d820b-124">Remarks</span></span>

<span data-ttu-id="d820b-125">A partir do SDK da série 9 do Windows Media Format, nenhum novo perfil de sistema foi definido.</span><span class="sxs-lookup"><span data-stu-id="d820b-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="d820b-126">Somente os GUIDs do perfil do sistema da versão 8 (ou anterior) podem ser usados com esse método.</span><span class="sxs-lookup"><span data-stu-id="d820b-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="d820b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d820b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d820b-128">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d820b-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

