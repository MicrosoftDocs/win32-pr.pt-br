---
description: O getownerid&\# 8194; O método de classe WMI recupera o SID (identificador de segurança) para o proprietário desse processo.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Método getownerid da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755197"
---
# <a name="getownersid-method-of-the-win32_process-class"></a><span data-ttu-id="c5541-103">Método getownerid da classe de \_ processo do Win32</span><span class="sxs-lookup"><span data-stu-id="c5541-103">GetOwnerSid method of the Win32\_Process class</span></span>

<span data-ttu-id="c5541-104">O método de classe **Getownerid** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) recupera o Sid (identificador de segurança) para o proprietário desse processo.</span><span class="sxs-lookup"><span data-stu-id="c5541-104">The **GetOwnerSid** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the security identifier (SID) for the owner of this process.</span></span>

<span data-ttu-id="c5541-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c5541-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c5541-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c5541-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5541-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5541-107">Syntax</span></span>


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a><span data-ttu-id="c5541-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5541-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5541-109">*Sid* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c5541-109">*Sid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5541-110">Retorna o descritor do identificador de segurança para este processo.</span><span class="sxs-lookup"><span data-stu-id="c5541-110">Returns the security identifier descriptor for this process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5541-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5541-111">Return value</span></span>

<span data-ttu-id="c5541-112">Retorna zero (0) para indicar êxito.</span><span class="sxs-lookup"><span data-stu-id="c5541-112">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="c5541-113">Qualquer outro número indica um erro.</span><span class="sxs-lookup"><span data-stu-id="c5541-113">Any other number indicates an error.</span></span> <span data-ttu-id="c5541-114">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c5541-114">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c5541-115">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c5541-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c5541-116">**Conclusão bem-sucedida** (0)</span><span class="sxs-lookup"><span data-stu-id="c5541-116">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-117">**Acesso negado** (2)</span><span class="sxs-lookup"><span data-stu-id="c5541-117">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-118">**Privilégio insuficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="c5541-118">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-119">**Falha desconhecida** (8)</span><span class="sxs-lookup"><span data-stu-id="c5541-119">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-120">**Caminho não encontrado** (9)</span><span class="sxs-lookup"><span data-stu-id="c5541-120">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-121">**Parâmetro inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="c5541-121">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="c5541-122">**Outro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="c5541-122">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="c5541-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5541-123">Examples</span></span>

<span data-ttu-id="c5541-124">O exemplo de código do PowerShell [localizar os usuários conectados em um sistema remoto/s versão 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) consulta computadores remotos para ver quem está conectado.</span><span class="sxs-lookup"><span data-stu-id="c5541-124">The [Find the logged on users on a remote system/s version 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell code example queries remote machines to see who is logged on.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5541-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5541-125">Requirements</span></span>



| <span data-ttu-id="c5541-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5541-126">Requirement</span></span> | <span data-ttu-id="c5541-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c5541-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5541-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5541-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c5541-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5541-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5541-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5541-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c5541-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5541-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5541-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5541-132">Namespace</span></span><br/>                | <span data-ttu-id="c5541-133">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c5541-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5541-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c5541-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5541-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5541-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5541-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c5541-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5541-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5541-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5541-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5541-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5541-139">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5541-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c5541-140">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="c5541-140">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

