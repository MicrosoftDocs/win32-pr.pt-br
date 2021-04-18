---
description: Salva os dados do filtro em um determinado fluxo.
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: Método CPersistStream. Save (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771844"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="d9dd7-103">Método CPersistStream. Save</span><span class="sxs-lookup"><span data-stu-id="d9dd7-103">CPersistStream.Save method</span></span>

<span data-ttu-id="d9dd7-104">Salva os dados do filtro em um determinado fluxo.</span><span class="sxs-lookup"><span data-stu-id="d9dd7-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9dd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d9dd7-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="d9dd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9dd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9dd7-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="d9dd7-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="d9dd7-108">Ponteiro para o fluxo no qual os dados serão salvos.</span><span class="sxs-lookup"><span data-stu-id="d9dd7-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="d9dd7-109">*fClearDirty*</span><span class="sxs-lookup"><span data-stu-id="d9dd7-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="d9dd7-110">Sinalizador que indica se o sinalizador sujo do fluxo atual deve ser redefinido; **Verdadeiro** significa redefini-lo.</span><span class="sxs-lookup"><span data-stu-id="d9dd7-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="d9dd7-111">(Quando o método é chamado como parte de uma operação de salvamento, o valor normalmente é **true**; quando chamado como parte de uma operação salvar como, o valor normalmente é **false**.)</span><span class="sxs-lookup"><span data-stu-id="d9dd7-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9dd7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9dd7-112">Return value</span></span>

<span data-ttu-id="d9dd7-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9dd7-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9dd7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9dd7-114">Remarks</span></span>

<span data-ttu-id="d9dd7-115">Essa função de membro implementa o método **IPersistStream:: Save** .</span><span class="sxs-lookup"><span data-stu-id="d9dd7-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="d9dd7-116">Ele chama **WriteInt** com a versão do software, [**chama CPersistStream:: WriteToStream**](cpersiststream-writetostream.md) com o fluxo em *pStm* e redefine **mPS \_ fDirty**.</span><span class="sxs-lookup"><span data-stu-id="d9dd7-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9dd7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9dd7-117">Requirements</span></span>



| <span data-ttu-id="d9dd7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9dd7-118">Requirement</span></span> | <span data-ttu-id="d9dd7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d9dd7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dd7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9dd7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d9dd7-121"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd7-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9dd7-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9dd7-122">Library</span></span><br/> | <dl> <span data-ttu-id="d9dd7-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d9dd7-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9dd7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9dd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9dd7-125">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="d9dd7-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




