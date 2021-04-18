---
title: Método IWMDRMLicense GetOutputProtectionLevels
description: O método GetOutputProtectionLevels recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Formato de mídia do Windows do método GetOutputProtectionLevels
- Método GetOutputProtectionLevels Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105813679"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="a3d2c-106">Método IWMDRMLicense:: GetOutputProtectionLevels</span><span class="sxs-lookup"><span data-stu-id="a3d2c-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="a3d2c-107">O método **GetOutputProtectionLevels** recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.</span><span class="sxs-lookup"><span data-stu-id="a3d2c-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d2c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d2c-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="a3d2c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d2c-110">*pOPLs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3d2c-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d2c-111">Ponteiro para uma estrutura de níveis de proteção de saída do WMDRM que recebe as informações de OPL. [**\_ \_ \_**](wmdrm-output-protection-levels.md)</span><span class="sxs-lookup"><span data-stu-id="a3d2c-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d2c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3d2c-112">Return value</span></span>

<span data-ttu-id="a3d2c-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a3d2c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a3d2c-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3d2c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a3d2c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a3d2c-115">Return code</span></span>                                                                          | <span data-ttu-id="a3d2c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3d2c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a3d2c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3d2c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a3d2c-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a3d2c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3d2c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3d2c-119">Remarks</span></span>

<span data-ttu-id="a3d2c-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a3d2c-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3d2c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3d2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d2c-122">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="a3d2c-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





