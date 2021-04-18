---
description: Nome do PIN.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membro CBasePin:: m_pName (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751706"
---
# <a name="cbasepinm_pname-member"></a><span data-ttu-id="b45be-103">Membro de CBasePin:: m \_ pname</span><span class="sxs-lookup"><span data-stu-id="b45be-103">CBasePin::m\_pName member</span></span>

<span data-ttu-id="b45be-104">Nome do PIN.</span><span class="sxs-lookup"><span data-stu-id="b45be-104">Pin name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b45be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b45be-105">Syntax</span></span>


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a><span data-ttu-id="b45be-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="b45be-106">Remarks</span></span>

<span data-ttu-id="b45be-107">O método [**CBasePin:: QueryPinInfo**](cbasepin-querypininfo.md) retorna essa cadeia de caracteres como o nome do PIN e o método [**CBasePin:: QueryId**](cbasepin-queryid.md) o retorna como o identificador do PIN.</span><span class="sxs-lookup"><span data-stu-id="b45be-107">The [**CBasePin::QueryPinInfo**](cbasepin-querypininfo.md) method returns this string as the pin name, and the [**CBasePin::QueryId**](cbasepin-queryid.md) method returns it as the pin identifier.</span></span> <span data-ttu-id="b45be-108">Em geral, no entanto, o nome do PIN e o identificador do PIN não precisam ser os mesmos.</span><span class="sxs-lookup"><span data-stu-id="b45be-108">In general, however, the pin name and the pin identifier are not required to be the same.</span></span> <span data-ttu-id="b45be-109">O identificador de PIN é usado para persistência de gráfico.</span><span class="sxs-lookup"><span data-stu-id="b45be-109">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="b45be-110">Para obter mais informações, consulte [**IBaseFilter:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span><span class="sxs-lookup"><span data-stu-id="b45be-110">For more information, see [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).</span></span>

## <a name="requirements"></a><span data-ttu-id="b45be-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b45be-111">Requirements</span></span>



| <span data-ttu-id="b45be-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b45be-112">Requirement</span></span> | <span data-ttu-id="b45be-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b45be-113">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b45be-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b45be-114">Header</span></span><br/> | <dl> <span data-ttu-id="b45be-115"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b45be-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b45be-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="b45be-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b45be-117">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b45be-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




