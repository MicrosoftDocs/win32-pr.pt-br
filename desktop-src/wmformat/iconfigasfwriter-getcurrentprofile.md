---
title: Método IConfigAsfWriter GetCurrentProfile
description: O método GetCurrentProfile recupera o perfil definido pelo aplicativo.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Formato de mídia do Windows do método GetCurrentProfile
- Método GetCurrentProfile Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105768352"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="29096-106">Método IConfigAsfWriter:: GetCurrentProfile</span><span class="sxs-lookup"><span data-stu-id="29096-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="29096-107">O método **GetCurrentProfile** recupera o perfil definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="29096-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="29096-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29096-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="29096-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29096-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29096-110">*ppProfile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="29096-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29096-111">Endereço de um ponteiro que recebe a interface [**IWMProfile**](iwmprofile.md) do perfil definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="29096-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29096-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29096-112">Return value</span></span>

<span data-ttu-id="29096-113">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29096-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="29096-114">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29096-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="29096-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="29096-115">Remarks</span></span>

<span data-ttu-id="29096-116">Se o método tiver sucesso, o ponteiro **IWMProfile** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="29096-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="29096-117">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="29096-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="29096-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="29096-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="29096-119">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="29096-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 