---
description: Define o mapeamento de sub-amostra para o exemplo que indica os bytes claros e criptografados nos dados de exemplo.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Atributo MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795458"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="7877b-103">Atributo MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit</span><span class="sxs-lookup"><span data-stu-id="7877b-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="7877b-104">Define o mapeamento de sub-amostra para o exemplo que indica os bytes claros e criptografados nos dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="7877b-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="7877b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7877b-105">Data type</span></span>

<span data-ttu-id="7877b-106">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="7877b-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="7877b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7877b-107">Remarks</span></span>

<span data-ttu-id="7877b-108">O **blob** deve conter uma matriz de intervalos de bytes como DWORDs onde cada duas DWORDs faz um conjunto.</span><span class="sxs-lookup"><span data-stu-id="7877b-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="7877b-109">A primeira DWORD de cada conjunto é o número de bytes claros e a segunda DWORD do conjunto é o número de bytes criptografados.</span><span class="sxs-lookup"><span data-stu-id="7877b-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="7877b-110">Observe que um par de 0s não é um conjunto válido (ambos os valores podem ser 0, mas não ambos).</span><span class="sxs-lookup"><span data-stu-id="7877b-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="7877b-111">A matriz de intervalos de bytes indica quais intervalos devem ser descriptografados, incluindo a possibilidade de que o exemplo inteiro não seja descriptografado.</span><span class="sxs-lookup"><span data-stu-id="7877b-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="7877b-112">É recomendável que isso não seja definido em amostras claras, embora seja possível obter o mesmo resultado definindo-o com os valores apropriados.</span><span class="sxs-lookup"><span data-stu-id="7877b-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="7877b-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7877b-113">Examples</span></span>

<span data-ttu-id="7877b-114">O exemplo a seguir mostra como definir MFSampleExtension de \_ criptografia \_ SubSampleMappingSplit.</span><span class="sxs-lookup"><span data-stu-id="7877b-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="7877b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7877b-115">Requirements</span></span>



| <span data-ttu-id="7877b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7877b-116">Requirement</span></span> | <span data-ttu-id="7877b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7877b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7877b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7877b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7877b-119">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7877b-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7877b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7877b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7877b-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7877b-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7877b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7877b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7877b-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7877b-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7877b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7877b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7877b-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7877b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7877b-126">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="7877b-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="7877b-127">\_Keyid conteúdo do MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="7877b-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




