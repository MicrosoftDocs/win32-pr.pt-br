---
description: Obtém uma referência a um objeto de driver TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Função ReferenceTcpDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751948"
---
# <a name="referencetcpdriver-function"></a><span data-ttu-id="efe1c-103">Função ReferenceTcpDriver</span><span class="sxs-lookup"><span data-stu-id="efe1c-103">ReferenceTcpDriver function</span></span>

<span data-ttu-id="efe1c-104">Obtém uma referência a um objeto de driver TCP v4.</span><span class="sxs-lookup"><span data-stu-id="efe1c-104">Obtains a reference to a TCP v4 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efe1c-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="efe1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efe1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe1c-107">*ppDriverObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="efe1c-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efe1c-108">Um ponteiro para uma estrutura de **\_ objeto de driver** .</span><span class="sxs-lookup"><span data-stu-id="efe1c-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="efe1c-109">Para obter mais informações, consulte a documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="efe1c-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe1c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efe1c-110">Return value</span></span>

<span data-ttu-id="efe1c-111">Se a função for bem-sucedida, ela retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="efe1c-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="efe1c-112">Se falhar, ele retornará o código de status apropriado.</span><span class="sxs-lookup"><span data-stu-id="efe1c-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe1c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe1c-113">Remarks</span></span>

<span data-ttu-id="efe1c-114">Essa função pode ser chamada somente do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="efe1c-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="efe1c-115">O chamador deve decrementar a contagem de referência chamando a função **ObDereferenceObject** quando terminar com o objeto.</span><span class="sxs-lookup"><span data-stu-id="efe1c-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="efe1c-116">Essa função é implementada em Drvref. lib, que está disponível para download.</span><span class="sxs-lookup"><span data-stu-id="efe1c-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="efe1c-117">Consulte [biblioteca de API de referência do driver de rede do Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="efe1c-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="efe1c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efe1c-118">Requirements</span></span>



| <span data-ttu-id="efe1c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="efe1c-119">Requirement</span></span> | <span data-ttu-id="efe1c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="efe1c-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efe1c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="efe1c-121">Library</span></span><br/> | <dl> <span data-ttu-id="efe1c-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efe1c-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe1c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe1c-124">**ReferenceTcpDriverV6**</span><span class="sxs-lookup"><span data-stu-id="efe1c-124">**ReferenceTcpDriverV6**</span></span>](referencetcpdriverv6.md)
</dt> </dl>

 

 




