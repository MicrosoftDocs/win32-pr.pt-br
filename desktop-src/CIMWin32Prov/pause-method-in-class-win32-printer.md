---
description: Pausa a fila de impressão.
ms.assetid: 0f425318-a7c0-4bba-bb44-e7635fa3ca03
ms.tgt_platform: multiple
title: Método Pause da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12d7e84351d77730b580242a58b38d7506af451a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370492"
---
# <a name="pause-method-of-the-win32_printer-class"></a><span data-ttu-id="c698a-103">Método Pause da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="c698a-103">Pause method of the Win32\_Printer class</span></span>

<span data-ttu-id="c698a-104">O método **Pause** [WMI da classe](/windows/desktop/WmiSdk/retrieving-a-class) pausa a fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="c698a-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method pauses the print queue.</span></span> <span data-ttu-id="c698a-105">Nenhum trabalho pode ser impresso até que a fila seja retomada.</span><span class="sxs-lookup"><span data-stu-id="c698a-105">No jobs can print until the queue is resumed.</span></span>

<span data-ttu-id="c698a-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c698a-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c698a-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c698a-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c698a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c698a-108">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="c698a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c698a-109">Parameters</span></span>

<span data-ttu-id="c698a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c698a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c698a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c698a-111">Return value</span></span>

<span data-ttu-id="c698a-112">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c698a-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="c698a-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c698a-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c698a-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c698a-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c698a-115">**0**</span><span class="sxs-lookup"><span data-stu-id="c698a-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c698a-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="c698a-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="c698a-117">**5**</span><span class="sxs-lookup"><span data-stu-id="c698a-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="c698a-118">Acesso negado</span><span class="sxs-lookup"><span data-stu-id="c698a-118">Access Denied</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c698a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c698a-119">Requirements</span></span>



| <span data-ttu-id="c698a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c698a-120">Requirement</span></span> | <span data-ttu-id="c698a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c698a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c698a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c698a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c698a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c698a-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c698a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c698a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c698a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c698a-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c698a-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c698a-126">Namespace</span></span><br/>                | <span data-ttu-id="c698a-127">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c698a-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="c698a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="c698a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c698a-129"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="c698a-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="c698a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c698a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c698a-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c698a-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c698a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="c698a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c698a-133">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="c698a-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c698a-134">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="c698a-134">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="c698a-135">**Método Resume**</span><span class="sxs-lookup"><span data-stu-id="c698a-135">**Resume method**</span></span>](resume-method-in-class-win32-printer.md)
</dt> </dl>

 

