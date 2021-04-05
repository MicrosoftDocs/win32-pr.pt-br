---
title: Método SetEncryptionLevel da classe Win32_TSGeneralSetting
description: O método SetEncryptionLevel define o nível de criptografia.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetEncryptionLevel
- Método SetEncryptionLevel Serviços de Área de Trabalho Remota, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Serviços de Área de Trabalho Remota, método SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085861"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="78fe5-106">Método SetEncryptionLevel da classe Win32 \_ TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="78fe5-106">SetEncryptionLevel method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="78fe5-107">O método **SetEncryptionLevel** define o nível de criptografia.</span><span class="sxs-lookup"><span data-stu-id="78fe5-107">The **SetEncryptionLevel** method sets the encryption level.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fe5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78fe5-108">Syntax</span></span>


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a><span data-ttu-id="78fe5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78fe5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78fe5-110">*MinEncryptionLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78fe5-110">*MinEncryptionLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78fe5-111">O nível de criptografia mínimo a ser definido.</span><span class="sxs-lookup"><span data-stu-id="78fe5-111">The minimum encryption level to set.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="78fe5-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="78fe5-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="78fe5-113">Nível baixo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="78fe5-113">Low level of encryption.</span></span> <span data-ttu-id="78fe5-114">Somente os dados enviados do cliente para o servidor são criptografados usando a criptografia de 56 bits.</span><span class="sxs-lookup"><span data-stu-id="78fe5-114">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="78fe5-115">Observe que os dados enviados do servidor para o cliente não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="78fe5-115">Note that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="78fe5-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="78fe5-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="78fe5-117">Nível de criptografia compatível com o cliente.</span><span class="sxs-lookup"><span data-stu-id="78fe5-117">Client-compatible level of encryption.</span></span> <span data-ttu-id="78fe5-118">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados na força de chave máxima com suporte do cliente.</span><span class="sxs-lookup"><span data-stu-id="78fe5-118">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="78fe5-119"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="78fe5-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="78fe5-120">Alto nível de criptografia.</span><span class="sxs-lookup"><span data-stu-id="78fe5-120">High level of encryption.</span></span> <span data-ttu-id="78fe5-121">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados usando criptografia de 128 bits de alta segurança.</span><span class="sxs-lookup"><span data-stu-id="78fe5-121">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="78fe5-122">Os clientes que não dão suporte a esse nível de criptografia não podem se conectar.</span><span class="sxs-lookup"><span data-stu-id="78fe5-122">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="78fe5-123"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="78fe5-123"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="78fe5-124">Criptografia em conformidade com FIPS.</span><span class="sxs-lookup"><span data-stu-id="78fe5-124">FIPS-compliant encryption.</span></span> <span data-ttu-id="78fe5-125">Todos os dados enviados do cliente para o servidor e do servidor para o cliente são criptografados e descriptografados com os algoritmos de criptografia do padrão FIPS (FIPS) usando os módulos criptográficos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78fe5-125">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="78fe5-126">O FIPS é um padrão intitulado "requisitos de segurança para módulos criptográficos".</span><span class="sxs-lookup"><span data-stu-id="78fe5-126">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="78fe5-127">O FIPS 140-1 (1994) e o FIPS 140-2 (2001) descrevem os requisitos governamentais dos módulos de criptografia de hardware e software usados no governo dos EUA.</span><span class="sxs-lookup"><span data-stu-id="78fe5-127">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78fe5-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78fe5-128">Return value</span></span>

<span data-ttu-id="78fe5-129">Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="78fe5-129">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="78fe5-130">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="78fe5-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="78fe5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="78fe5-131">Remarks</span></span>

<span data-ttu-id="78fe5-132">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="78fe5-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="78fe5-133">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="78fe5-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="78fe5-134">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="78fe5-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="78fe5-135">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="78fe5-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="78fe5-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78fe5-136">Requirements</span></span>



| <span data-ttu-id="78fe5-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="78fe5-137">Requirement</span></span> | <span data-ttu-id="78fe5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="78fe5-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78fe5-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78fe5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="78fe5-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78fe5-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78fe5-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78fe5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="78fe5-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78fe5-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78fe5-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="78fe5-143">Namespace</span></span><br/>                | <span data-ttu-id="78fe5-144">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="78fe5-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="78fe5-145">MOF</span><span class="sxs-lookup"><span data-stu-id="78fe5-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78fe5-146"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78fe5-146"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78fe5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="78fe5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78fe5-148"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78fe5-148"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78fe5-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="78fe5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fe5-150">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="78fe5-150">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

