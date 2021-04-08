---
title: Atributo v1_enum
description: O atributo \ v1 \_ enum \ é direcionado que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum do atributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823279"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="361c7-104">\_atributo de enumeração v1</span><span class="sxs-lookup"><span data-stu-id="361c7-104">v1\_enum attribute</span></span>

<span data-ttu-id="361c7-105">O atributo de **\[ \_ enumeração \] v1** direciona que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="361c7-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="361c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="361c7-106">Parameters</span></span>

<span data-ttu-id="361c7-107">Este atributo não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="361c7-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="361c7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="361c7-108">Remarks</span></span>

<span data-ttu-id="361c7-109">Usar o atributo de **\[ \_ enumeração \] v1** para transmitir um tipo enumerado como uma entidade de 32 bits aumenta a eficiência do marshaling e o desempacotamento de dados quando tal enumeração é inserida em estruturas ou uniões.</span><span class="sxs-lookup"><span data-stu-id="361c7-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="361c7-110">Para melhorar o desempenho, é recomendável aplicar o atributo de **\[ \_ enumeração \] v1** a enumeradores em aplicativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="361c7-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="361c7-111">No entanto, tenha em mente que, em plataformas de 16 bits, o compilador C trata um tipo enumerado como um [**int**](int.md)de 16 bits. Portanto, os aplicativos cliente de 16 bits precisam converter os tipos de [**Enumeração**](enum.md) [**para a transmissão**](long.md) remota a fim de evitar a substituição de dados ou o envio de valores incorretos.</span><span class="sxs-lookup"><span data-stu-id="361c7-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="361c7-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="361c7-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="361c7-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="361c7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361c7-114">**enumera**</span><span class="sxs-lookup"><span data-stu-id="361c7-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="361c7-115">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="361c7-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="361c7-116">**Longas**</span><span class="sxs-lookup"><span data-stu-id="361c7-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




