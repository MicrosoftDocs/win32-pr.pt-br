---
description: Contém um valor de polaridade a ser retornado.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Estrutura de PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920314"
---
# <a name="pwm_pin_get_polarity_output-structure"></a><span data-ttu-id="a9a3b-103">PWM \_ PIN \_ obter a \_ estrutura de saída de polaridade \_</span><span class="sxs-lookup"><span data-stu-id="a9a3b-103">PWM\_PIN\_GET\_POLARITY\_OUTPUT structure</span></span>

<span data-ttu-id="a9a3b-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a9a3b-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="a9a3b-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a9a3b-106">Contém um valor de polaridade a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-106">Contains a polarity value to return.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a3b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9a3b-107">Syntax</span></span>


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="a9a3b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a9a3b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9a3b-109">**Polaridade**</span><span class="sxs-lookup"><span data-stu-id="a9a3b-109">**Polarity**</span></span>
</dt> <dd>

<span data-ttu-id="a9a3b-110">A polaridade do PIN ou canal como um valor de [**\_ polaridade PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .</span><span class="sxs-lookup"><span data-stu-id="a9a3b-110">The polarity of the pin or channel as a [**PWM\_POLARITY**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) value.</span></span> <span data-ttu-id="a9a3b-111">A polaridade é ativo alto ou ativo baixo.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-111">The polarity is either Active High or Active Low.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9a3b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9a3b-112">Requirements</span></span>



| <span data-ttu-id="a9a3b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a3b-113">Requirement</span></span> | <span data-ttu-id="a9a3b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a9a3b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a3b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a3b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a9a3b-116">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a9a3b-116">Windows 10 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9a3b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9a3b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a9a3b-118">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a9a3b-118">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a9a3b-119">Versão mínima do KMDF</span><span class="sxs-lookup"><span data-stu-id="a9a3b-119">Minimum KMDF version</span></span><br/>     | <span data-ttu-id="a9a3b-120">1,19</span><span class="sxs-lookup"><span data-stu-id="a9a3b-120">1.19</span></span><br/>                                                                                  |
| <span data-ttu-id="a9a3b-121">Versão mínima do UMDF</span><span class="sxs-lookup"><span data-stu-id="a9a3b-121">Minimum UMDF version</span></span><br/>     | <span data-ttu-id="a9a3b-122">2.19</span><span class="sxs-lookup"><span data-stu-id="a9a3b-122">2.19</span></span><br/>                                                                                  |
| <span data-ttu-id="a9a3b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9a3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9a3b-124"><dt>PWM. h (incluir PWM. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a3b-124"><dt>Pwm.h (include Pwm.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a3b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9a3b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a3b-126">**IOCTL \_ PWM \_ PIN \_ obter \_ polaridade**</span><span class="sxs-lookup"><span data-stu-id="a9a3b-126">**IOCTL\_PWM\_PIN\_GET\_POLARITY**</span></span>](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[<span data-ttu-id="a9a3b-127">**\_polaridade PWM**</span><span class="sxs-lookup"><span data-stu-id="a9a3b-127">**PWM\_POLARITY**</span></span>](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

