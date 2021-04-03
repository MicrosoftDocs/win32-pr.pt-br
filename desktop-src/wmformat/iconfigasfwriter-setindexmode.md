---
title: Método setindexmode de IConfigAsfWriter
description: O método setindexmode permite que o aplicativo controle se o arquivo será indexado de forma temporal.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Método setindexmode formato de mídia do Windows
- Método setindexmode formato de mídia do Windows, interface IConfigAsfWriter
- IConfigAsfWriter interface formato Windows Media, método setindexmode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007594"
---
# <a name="iconfigasfwritersetindexmode-method"></a><span data-ttu-id="abc84-106">Método IConfigAsfWriter:: setindexmode</span><span class="sxs-lookup"><span data-stu-id="abc84-106">IConfigAsfWriter::SetIndexMode method</span></span>

<span data-ttu-id="abc84-107">O método **Setindexmode** permite que o aplicativo controle se o arquivo será indexado de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="abc84-107">The **SetIndexMode** method enables the application to control whether the file will be temporally indexed.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc84-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abc84-108">Syntax</span></span>


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a><span data-ttu-id="abc84-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abc84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc84-110">*bIndexFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="abc84-110">*bIndexFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abc84-111">Variável do tipo **bool**; **True** especifica que o arquivo será indexado de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="abc84-111">Variable of type **BOOL**; **TRUE** specifies that the file will be temporally indexed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc84-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abc84-112">Return value</span></span>

<span data-ttu-id="abc84-113">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="abc84-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="abc84-114">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="abc84-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="abc84-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="abc84-115">Remarks</span></span>

<span data-ttu-id="abc84-116">Por padrão, o [gravador ASF do WM](wm-asf-writer-filter.md) cria arquivos ASF indexados de temporal.</span><span class="sxs-lookup"><span data-stu-id="abc84-116">By default, the [WM ASF Writer](wm-asf-writer-filter.md) creates temporally indexed ASF files.</span></span> <span data-ttu-id="abc84-117">Ele executa a indexação quando o grafo para.</span><span class="sxs-lookup"><span data-stu-id="abc84-117">It performs the indexing when the graph stops.</span></span> <span data-ttu-id="abc84-118">Você pode desabilitar esse comportamento se quiser fazer sua própria indexação baseada em quadros como uma etapa de pós-processamento.</span><span class="sxs-lookup"><span data-stu-id="abc84-118">You can disable this behavior if you want to do your own frame-based indexing as a post-processing step.</span></span> <span data-ttu-id="abc84-119">Para criar um arquivo indexado por quadro, chame **Setindexmode**(false), crie o arquivo e, em seguida, use os métodos do Windows Media Format SDK diretamente para criar um índice baseado em quadro para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="abc84-119">To create a frame-indexed file, call **SetIndexMode**(FALSE), create the file, and then use the Windows Media Format SDK methods directly to create a frame-based index for the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="abc84-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="abc84-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="abc84-121">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="abc84-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 