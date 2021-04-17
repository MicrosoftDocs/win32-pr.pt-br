---
description: Obtém uma referência a um objeto de driver TCP v6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: Função ReferenceTcpDriverV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749708"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="9e427-103">Função ReferenceTcpDriverV6</span><span class="sxs-lookup"><span data-stu-id="9e427-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="9e427-104">Obtém uma referência a um objeto de driver TCP v6.</span><span class="sxs-lookup"><span data-stu-id="9e427-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e427-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e427-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="9e427-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e427-107">*ppDriverObject* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9e427-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e427-108">Um ponteiro para uma estrutura de **\_ objeto de driver** .</span><span class="sxs-lookup"><span data-stu-id="9e427-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="9e427-109">Para obter mais informações, consulte a documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="9e427-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e427-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e427-110">Return value</span></span>

<span data-ttu-id="9e427-111">Se a função for bem-sucedida, ela retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="9e427-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="9e427-112">Se falhar, ele retornará o código de status apropriado.</span><span class="sxs-lookup"><span data-stu-id="9e427-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e427-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e427-113">Remarks</span></span>

<span data-ttu-id="9e427-114">Essa função pode ser chamada somente do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="9e427-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="9e427-115">O chamador deve decrementar a contagem de referência chamando a função **ObDereferenceObject** quando terminar com o objeto.</span><span class="sxs-lookup"><span data-stu-id="9e427-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="9e427-116">Essa função é implementada em Drvref. lib, que está disponível para download.</span><span class="sxs-lookup"><span data-stu-id="9e427-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="9e427-117">Consulte [biblioteca de API de referência do driver de rede do Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="9e427-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e427-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e427-118">Requirements</span></span>



| <span data-ttu-id="9e427-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e427-119">Requirement</span></span> | <span data-ttu-id="9e427-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9e427-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e427-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e427-121">Library</span></span><br/> | <dl> <span data-ttu-id="9e427-122"><dt>Drvref. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e427-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e427-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e427-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e427-124">**ReferenceTcpDriver**</span><span class="sxs-lookup"><span data-stu-id="9e427-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




