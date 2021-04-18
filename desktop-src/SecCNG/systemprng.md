---
description: Recupera um número especificado de bytes aleatórios do gerador de número aleatório do sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Função SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758925"
---
# <a name="systemprng-function"></a><span data-ttu-id="c6a84-103">Função SystemPrng</span><span class="sxs-lookup"><span data-stu-id="c6a84-103">SystemPrng function</span></span>

<span data-ttu-id="c6a84-104">\[O **SystemPrng** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c6a84-104">\[**SystemPrng** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c6a84-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c6a84-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c6a84-106">Em vez disso, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span><span class="sxs-lookup"><span data-stu-id="c6a84-106">Instead, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]</span></span>

<span data-ttu-id="c6a84-107">A função **SystemPrng** recupera um número especificado de bytes aleatórios do gerador de números aleatórios do sistema.</span><span class="sxs-lookup"><span data-stu-id="c6a84-107">The **SystemPrng** function retrieves a specified number of random bytes from the system random number generator.</span></span>

> [!Note]  
> <span data-ttu-id="c6a84-108">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="c6a84-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="c6a84-109">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c6a84-109">To call this function, you must create a user-defined header file.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c6a84-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6a84-110">Syntax</span></span>


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a><span data-ttu-id="c6a84-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6a84-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a84-112">*pbRandomData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c6a84-112">*pbRandomData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a84-113">Um ponteiro para um buffer que recebe os bytes recuperados.</span><span class="sxs-lookup"><span data-stu-id="c6a84-113">A pointer to a buffer that receives the retrieved bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c6a84-114">*cbRandomData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6a84-114">*cbRandomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6a84-115">O número de bytes a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="c6a84-115">The number of bytes to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a84-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6a84-116">Return value</span></span>

<span data-ttu-id="c6a84-117">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="c6a84-117">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a84-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6a84-118">Requirements</span></span>



| <span data-ttu-id="c6a84-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a84-119">Requirement</span></span> | <span data-ttu-id="c6a84-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c6a84-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a84-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6a84-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a84-122">\[Somente aplicativos da área de trabalho do Windows Vista com SP1\]</span><span class="sxs-lookup"><span data-stu-id="c6a84-122">Windows Vista with SP1 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                        |
| <span data-ttu-id="c6a84-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6a84-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a84-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6a84-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                           |
| <span data-ttu-id="c6a84-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c6a84-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6a84-126"><dt>Ksecdd.sys no Windows Server 2008 e no Windows Vista com SP1; </dt> <dt>Cng.sys no Windows 7 e no Windows Server 2008 R2</dt></span><span class="sxs-lookup"><span data-stu-id="c6a84-126"><dt>Ksecdd.sys on Windows Server 2008 and Windows Vista with SP1; </dt> <dt>Cng.sys on Windows 7 and Windows Server 2008 R2</dt></span></span> </dl> |



 

 




