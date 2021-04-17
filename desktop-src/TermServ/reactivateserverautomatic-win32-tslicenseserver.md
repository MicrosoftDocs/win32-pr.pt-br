---
title: Método ReactivateServerAutomatic da classe Win32_TSLicenseServer
description: Reativa o servidor de licença Área de Trabalho Remota usando uma conexão automática com a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReactivateServerAutomatic
- Método ReactivateServerAutomatic Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813027"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="d7ad9-106">Método ReactivateServerAutomatic da classe Win32 \_ TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="d7ad9-106">ReactivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="d7ad9-107">Reativa o servidor de licença Área de Trabalho Remota usando uma conexão automática com a Internet.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-107">Reactivates the Remote Desktop license server by using an automatic connection to the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ad9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7ad9-108">Syntax</span></span>


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d7ad9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7ad9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ad9-110">*Motivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7ad9-110">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-111">Motivo da ativação.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-111">Reason for the activation.</span></span> <span data-ttu-id="d7ad9-112">Pode ser um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-112">It can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d7ad9-113">0</span><span class="sxs-lookup"><span data-stu-id="d7ad9-113">0</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-114">O servidor foi reimplantado.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-114">The server was redeployed.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-115">1</span><span class="sxs-lookup"><span data-stu-id="d7ad9-115">1</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-116">O certificado foi corrompido.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-116">The certificate was corrupt.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-117">2</span><span class="sxs-lookup"><span data-stu-id="d7ad9-117">2</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-118">A chave privada foi comprometida.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-118">The private key was compromised.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-119">3</span><span class="sxs-lookup"><span data-stu-id="d7ad9-119">3</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-120">A chave de ativação expirou.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-120">The activation key expired.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-121">4</span><span class="sxs-lookup"><span data-stu-id="d7ad9-121">4</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-122">O servidor foi atualizado.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-122">The server was upgraded.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d7ad9-123">*ActivationStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d7ad9-123">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-124">O status de ativação retornado pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-124">The activation status returned can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d7ad9-125">0</span><span class="sxs-lookup"><span data-stu-id="d7ad9-125">0</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-126">O servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-126">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-127">1</span><span class="sxs-lookup"><span data-stu-id="d7ad9-127">1</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-128">O servidor de licença Área de Trabalho Remota não está ativado.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-128">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-129">2</span><span class="sxs-lookup"><span data-stu-id="d7ad9-129">2</span></span>
</dt> <dd>

<span data-ttu-id="d7ad9-130">Erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-130">An unknown error occurred.</span></span> <span data-ttu-id="d7ad9-131">Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-131">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ad9-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7ad9-132">Return value</span></span>

<span data-ttu-id="d7ad9-133">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-133">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d7ad9-134">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-134">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d7ad9-135">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d7ad9-135">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ad9-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7ad9-136">Remarks</span></span>

<span data-ttu-id="d7ad9-137">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-137">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d7ad9-138">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d7ad9-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d7ad9-139">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d7ad9-140">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d7ad9-141">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d7ad9-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ad9-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ad9-142">Requirements</span></span>



| <span data-ttu-id="d7ad9-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ad9-143">Requirement</span></span> | <span data-ttu-id="d7ad9-144">Valor</span><span class="sxs-lookup"><span data-stu-id="d7ad9-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ad9-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7ad9-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ad9-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d7ad9-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d7ad9-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7ad9-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ad9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7ad9-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d7ad9-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7ad9-149">Namespace</span></span><br/>                | <span data-ttu-id="d7ad9-150">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d7ad9-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d7ad9-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d7ad9-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7ad9-152"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7ad9-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7ad9-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d7ad9-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7ad9-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7ad9-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ad9-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7ad9-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ad9-156">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="d7ad9-156">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

