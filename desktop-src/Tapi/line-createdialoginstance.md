---
description: A mensagem TSPI LINE \_ CREATEDIALOGINSTANCE faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da \_ função TUISPI providerGenericDialog em execução no contexto do aplicativo.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Mensagem de LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753538"
---
# <a name="line_createdialoginstance-message"></a><span data-ttu-id="d4a9a-103">Mensagem de CREATEDIALOGINSTANCE de linha \_</span><span class="sxs-lookup"><span data-stu-id="d4a9a-103">LINE\_CREATEDIALOGINSTANCE message</span></span>

<span data-ttu-id="d4a9a-104">A mensagem **de \_ CREATEDIALOGINSTANCE da linha** TSPI faz com que a TAPI crie uma associação entre o provedor de serviços e uma instância da função [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) em execução no contexto do aplicativo que invocou a função TSPI assíncrona identificada pelo parâmetro *DwRequestID* da estrutura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) apontada por *lpTUISPICreateDialogInstanceParams*.</span><span class="sxs-lookup"><span data-stu-id="d4a9a-104">The TSPI **LINE\_CREATEDIALOGINSTANCE** message causes TAPI to create an association between the service provider and an instance of the [**TUISPI\_providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) function executing in the context of the application that invoked the asynchronous TSPI function identified by the *dwRequestID* parameter of the [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure pointed to by *lpTUISPICreateDialogInstanceParams*.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d4a9a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4a9a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a9a-106">*hProvider*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-106">*hProvider*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a9a-107">O ProviderHandle fornecido ao provedor de serviços como um parâmetro para [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span><span class="sxs-lookup"><span data-stu-id="d4a9a-107">The ProviderHandle supplied to the service provider as a parameter to [**TSPI\_providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).</span></span>

</dd> <dt>

<span data-ttu-id="d4a9a-108">*lpTUISPICreateDialogInstanceParams*</span><span class="sxs-lookup"><span data-stu-id="d4a9a-108">*lpTUISPICreateDialogInstanceParams*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a9a-109">Ponteiro para uma estrutura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .</span><span class="sxs-lookup"><span data-stu-id="d4a9a-109">Pointer to a [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4a9a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4a9a-110">Requirements</span></span>



| <span data-ttu-id="d4a9a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4a9a-111">Requirement</span></span> | <span data-ttu-id="d4a9a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d4a9a-112">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d4a9a-113">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d4a9a-113">TAPI version</span></span><br/> | <span data-ttu-id="d4a9a-114">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d4a9a-114">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d4a9a-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4a9a-115">Header</span></span><br/>       | <dl> <span data-ttu-id="d4a9a-116"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4a9a-116"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4a9a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4a9a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4a9a-118">**TSPI \_ providerEnumDevices**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-118">**TSPI\_providerEnumDevices**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[<span data-ttu-id="d4a9a-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span><span class="sxs-lookup"><span data-stu-id="d4a9a-119">**TUISPICREATEDIALOGINSTANCEPARAMS**</span></span>](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

