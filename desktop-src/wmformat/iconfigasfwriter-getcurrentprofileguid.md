---
title: Método IConfigAsfWriter GetCurrentProfileGuid
description: O método GetCurrentProfileGuid recupera o GUID de perfil do sistema de mídia do Windows atual.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Formato de mídia do Windows do método GetCurrentProfileGuid
- Método GetCurrentProfileGuid Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294390"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="c1efa-106">Método IConfigAsfWriter:: GetCurrentProfileGuid</span><span class="sxs-lookup"><span data-stu-id="c1efa-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="c1efa-107">O método **GetCurrentProfileGuid** recupera o GUID de perfil do sistema de mídia do Windows atual.</span><span class="sxs-lookup"><span data-stu-id="c1efa-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1efa-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1efa-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="c1efa-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1efa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1efa-110">*pProfileGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c1efa-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1efa-111">Ponteiro para uma variável do tipo **GUID** que identifica o perfil do sistema atual que está sendo usado pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="c1efa-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1efa-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1efa-112">Return value</span></span>

<span data-ttu-id="c1efa-113">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c1efa-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c1efa-114">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c1efa-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1efa-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1efa-115">Remarks</span></span>

<span data-ttu-id="c1efa-116">Esse método não é usado com perfis personalizados (incluindo todos os perfis que incluem fluxos que usam os codecs de áudio e vídeo do Windows Media), pois todos esses perfis são criados por aplicativos e não têm nenhum identificador GUID.</span><span class="sxs-lookup"><span data-stu-id="c1efa-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="c1efa-117">Se nenhum perfil do sistema for carregado, *pProfileGuid* será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c1efa-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1efa-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1efa-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1efa-119">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c1efa-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 