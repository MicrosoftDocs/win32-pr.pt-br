---
description: Define um cache de métrica de fonte do Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751217"
---
# <a name="script_cache"></a><span data-ttu-id="431a2-103">CACHE de SCRIPT \_</span><span class="sxs-lookup"><span data-stu-id="431a2-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="431a2-104">Define um cache de métrica de fonte do Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="431a2-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="431a2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="431a2-105">Remarks</span></span>

<span data-ttu-id="431a2-106">Esta é uma estrutura opaca.</span><span class="sxs-lookup"><span data-stu-id="431a2-106">This is an opaque structure.</span></span> <span data-ttu-id="431a2-107">O aplicativo deve alocar e reter uma \_ variável de cache de script para cada estilo de caractere usado.</span><span class="sxs-lookup"><span data-stu-id="431a2-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="431a2-108">A variável deve ser inicializada como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="431a2-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="431a2-109">Muitas funções de script assumem uma combinação de um identificador de contexto de dispositivo de hardware e uma variável de cache de SCRIPT \_ .</span><span class="sxs-lookup"><span data-stu-id="431a2-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="431a2-110">O Uniscribe primeiro tenta acessar dados de fonte usando a \_ variável de cache de script.</span><span class="sxs-lookup"><span data-stu-id="431a2-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="431a2-111">Ele inspeciona apenas o contexto do dispositivo de hardware se os dados necessários ainda não estiverem em cache.</span><span class="sxs-lookup"><span data-stu-id="431a2-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="431a2-112">O identificador de contexto do dispositivo de hardware pode ser passado para o Uniscribe como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="431a2-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="431a2-113">Se os dados exigidos pelo Uniscribe já estiverem em cache, o contexto do dispositivo não será acessado e a operação continuará normalmente.</span><span class="sxs-lookup"><span data-stu-id="431a2-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="431a2-114">Se o contexto do dispositivo for passado como **nulo** e o Uniscribe precisar acessá-lo por qualquer motivo, o Uniscribe retornará o código de erro E \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="431a2-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="431a2-115">Esse código é retornado rapidamente, permitindo que o aplicativo Evite chamadas [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) demoradas.</span><span class="sxs-lookup"><span data-stu-id="431a2-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="431a2-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="431a2-116">Examples</span></span>

<span data-ttu-id="431a2-117">O exemplo a seguir aplica-se a todas as funções que usam uma variável de cache de SCRIPT \_ e um identificador opcional para um contexto de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="431a2-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="431a2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431a2-118">Requirements</span></span>



| <span data-ttu-id="431a2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="431a2-119">Requirement</span></span> | <span data-ttu-id="431a2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="431a2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="431a2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431a2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="431a2-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="431a2-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="431a2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431a2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="431a2-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="431a2-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="431a2-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="431a2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="431a2-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="431a2-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431a2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="431a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431a2-128">Cancelar</span><span class="sxs-lookup"><span data-stu-id="431a2-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="431a2-129">Estruturas do Uniscribe</span><span class="sxs-lookup"><span data-stu-id="431a2-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="431a2-130">Cache</span><span class="sxs-lookup"><span data-stu-id="431a2-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
