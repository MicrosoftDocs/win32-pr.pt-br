---
title: Método getindexmode de IConfigAsfWriter
description: O método getindexmode recupera o modo de índice temporal atual.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Método getindexmode formato de mídia do Windows
- Método getindexmode formato de mídia do Windows, interface IConfigAsfWriter
- IConfigAsfWriter interface formato Windows Media, método getindexmode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366269"
---
# <a name="iconfigasfwritergetindexmode-method"></a><span data-ttu-id="5007c-106">Método IConfigAsfWriter:: getindexmode</span><span class="sxs-lookup"><span data-stu-id="5007c-106">IConfigAsfWriter::GetIndexMode method</span></span>

<span data-ttu-id="5007c-107">O método **Getindexmode** recupera o modo de índice temporal atual.</span><span class="sxs-lookup"><span data-stu-id="5007c-107">The **GetIndexMode** method retrieves the current temporal index mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5007c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5007c-108">Syntax</span></span>


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="5007c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5007c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5007c-110">*pbIndexFile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5007c-110">*pbIndexFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5007c-111">Ponteiro para uma variável do tipo **bool** que recebe a configuração do modo de índice temporal.</span><span class="sxs-lookup"><span data-stu-id="5007c-111">Pointer to a variable of type **BOOL** that receives the temporal index mode setting.</span></span> <span data-ttu-id="5007c-112">Um valor **true** indica que o gravador ASF do WM está configurado para gravar arquivos indexados de temporal.</span><span class="sxs-lookup"><span data-stu-id="5007c-112">A value of **TRUE** indicates that the WM ASF Writer is configured to write temporally indexed files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5007c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5007c-113">Return value</span></span>

<span data-ttu-id="5007c-114">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5007c-114">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="5007c-115">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5007c-115">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5007c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5007c-116">Remarks</span></span>

<span data-ttu-id="5007c-117">Use esse método para determinar se o [gravador ASF do WM](wm-asf-writer-filter.md) está configurado atualmente para gravar arquivos ASF indexados de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="5007c-117">Use this method to determine whether the [WM ASF Writer](wm-asf-writer-filter.md) is currently configured to write temporally indexed ASF files.</span></span> <span data-ttu-id="5007c-118">Para obter mais informações sobre arquivos indexados de forma temporal e estruturados em quadros, consulte os comentários para [**IConfigAsfWriter:: Setindexmode**](iconfigasfwriter-setindexmode.md).</span><span class="sxs-lookup"><span data-stu-id="5007c-118">For more information on temporally indexed and frame-indexed files, see the Remarks for [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5007c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5007c-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="5007c-120">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5007c-120">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 