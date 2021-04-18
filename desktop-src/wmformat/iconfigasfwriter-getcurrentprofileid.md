---
title: Método IConfigAsfWriter GetCurrentProfileId
description: O método GetCurrentProfileId recupera a ID do perfil atual. (Somente para perfis do Windows Media Format 4,0.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Formato de mídia do Windows do método GetCurrentProfileId
- Método GetCurrentProfileId Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105781630"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="ed060-107">Método IConfigAsfWriter:: GetCurrentProfileId</span><span class="sxs-lookup"><span data-stu-id="ed060-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="ed060-108">O método **GetCurrentProfileId** recupera a ID do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="ed060-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="ed060-109">(Somente para perfis do Windows Media Format 4,0.)</span><span class="sxs-lookup"><span data-stu-id="ed060-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed060-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed060-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="ed060-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed060-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed060-112">*pdwProfileId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed060-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed060-113">Ponteiro para uma variável do tipo **DWORD** que recebe a ID do perfil atual.</span><span class="sxs-lookup"><span data-stu-id="ed060-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed060-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed060-114">Return value</span></span>

<span data-ttu-id="ed060-115">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed060-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ed060-116">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed060-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed060-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed060-117">Remarks</span></span>

<span data-ttu-id="ed060-118">Este método agora é obsoleto porque ele pressupõe os perfis do SDK do Windows Media Format versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="ed060-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="ed060-119">Use [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) ou [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) em vez de identificar corretamente um perfil para a versão 7,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ed060-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed060-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed060-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed060-121">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed060-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 