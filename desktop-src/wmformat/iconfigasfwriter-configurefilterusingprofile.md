---
title: Método IConfigAsfWriter ConfigureFilterUsingProfile
description: O método ConfigureFilterUsingProfile é a maneira recomendada para definir um perfil. Ele configura o filtro para gravar um arquivo ASF com base no perfil definido pelo aplicativo especificado.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfile
- Método ConfigureFilterUsingProfile Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761092"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="ba40b-107">Método IConfigAsfWriter:: ConfigureFilterUsingProfile</span><span class="sxs-lookup"><span data-stu-id="ba40b-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="ba40b-108">O método **ConfigureFilterUsingProfile** é a maneira recomendada para definir um perfil.</span><span class="sxs-lookup"><span data-stu-id="ba40b-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="ba40b-109">Ele configura o filtro para gravar um arquivo ASF com base no perfil definido pelo aplicativo especificado.</span><span class="sxs-lookup"><span data-stu-id="ba40b-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba40b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba40b-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="ba40b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba40b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba40b-112">*pProfile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba40b-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba40b-113">Ponteiro para a interface [**IWMProfile**](iwmprofile.md) no perfil definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ba40b-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba40b-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba40b-114">Return value</span></span>

<span data-ttu-id="ba40b-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ba40b-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ba40b-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba40b-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ba40b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba40b-117">Return code</span></span>                                                                                         | <span data-ttu-id="ba40b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba40b-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="ba40b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba40b-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="ba40b-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ba40b-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="ba40b-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ba40b-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="ba40b-122">O ponteiro de interface **IWMProfile** não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba40b-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ba40b-123"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba40b-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="ba40b-124">O grafo foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="ba40b-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="ba40b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba40b-125">Remarks</span></span>

<span data-ttu-id="ba40b-126">Se for bem-sucedido, esse método fará com que um evento **\_ \_ alterado de grafo do EC** seja enviado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ba40b-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="ba40b-127">Use este método para configurar o gravador com um perfil personalizado do Windows Media 9 Series que você criou (ou carregou a partir de um arquivo. prx existente) usando os métodos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ba40b-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba40b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba40b-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba40b-129">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba40b-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

