---
title: Método IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configura um canal de comunicação entre o host e o sistema operacional convidado.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- StartCommunicationChannel do método virtual PC
- Método StartCommunicationChannel Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455682"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="3f10f-106">Método IVMVirtualMachine:: StartCommunicationChannel</span><span class="sxs-lookup"><span data-stu-id="3f10f-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="3f10f-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3f10f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3f10f-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3f10f-109">Configura um canal de comunicação entre o host e o sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="3f10f-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f10f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f10f-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="3f10f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f10f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f10f-112">*inHostEndpointType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f10f-113">Esse parâmetro deve ser **vmEndpoint \_ NamedPipe** (0).</span><span class="sxs-lookup"><span data-stu-id="3f10f-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="3f10f-114">*inHostEndPointName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f10f-115">O nome exclusivo do pipe.</span><span class="sxs-lookup"><span data-stu-id="3f10f-115">The unique pipe name.</span></span> <span data-ttu-id="3f10f-116">Essa cadeia de caracteres deve ter o seguinte formato: " \\ \\ . \\ pipe \\ *pipeName*".</span><span class="sxs-lookup"><span data-stu-id="3f10f-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="3f10f-117">A parte de *pipeName* do nome pode incluir qualquer caractere diferente de uma barra invertida, incluindo números e caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="3f10f-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="3f10f-118">A cadeia de caracteres do nome do pipe inteiro pode ter até 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3f10f-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="3f10f-119">Os nomes dos pipes não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3f10f-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="3f10f-120">*inGuestEndpointType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f10f-121">Esse parâmetro deve ser **vmEndpoint \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="3f10f-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="3f10f-122">*inGuestEndpointName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f10f-123">O número da porta na qual o servidor TCP no convidado está escutando.</span><span class="sxs-lookup"><span data-stu-id="3f10f-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f10f-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f10f-124">Return value</span></span>

<span data-ttu-id="3f10f-125">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3f10f-125">This method can return one of these values.</span></span>



| <span data-ttu-id="3f10f-126">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3f10f-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="3f10f-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f10f-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f10f-128"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="3f10f-129">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3f10f-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="3f10f-130"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="3f10f-131">O parâmetro *inHostEndpointType* não é **vmEndpoint \_ NamedPipe** (0) ou o parâmetro *inGuestEndpointType* não é **vmEndpoint \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="3f10f-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="3f10f-132"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3f10f-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="3f10f-133">O parâmetro *inHostEndPointName* ou *inGuestEndpointName* é **nulo** ou não é um valor válido.</span><span class="sxs-lookup"><span data-stu-id="3f10f-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="3f10f-134"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3f10f-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="3f10f-135">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3f10f-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="3f10f-136"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ identificador inválido do erro)**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="3f10f-137">Um identificador não é válido.</span><span class="sxs-lookup"><span data-stu-id="3f10f-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="3f10f-138"><dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="3f10f-139">Não há memória suficiente disponível para concluir esta solicitação.</span><span class="sxs-lookup"><span data-stu-id="3f10f-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="3f10f-140"><dt>**HRESULT \_ DO \_ Win32 (erro \_ não \_ pronto)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="3f10f-141">O sistema subjacente que ele usa para fornecer serviços de rede está sendo inicializado no momento.</span><span class="sxs-lookup"><span data-stu-id="3f10f-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3f10f-142"><dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="3f10f-143">O nome do pipe já está em uso.</span><span class="sxs-lookup"><span data-stu-id="3f10f-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="3f10f-144"><dt>**HRESULT \_ DO \_ Win32 (pipe de erro \_ \_ ocupado)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="3f10f-145">Um ou mais canais estão em execução e podem ser disponibilizados em breve.</span><span class="sxs-lookup"><span data-stu-id="3f10f-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="3f10f-146"><dt>**HRESULT \_ Do \_ Win32 (máximo de sessões de erro \_ \_ \_ atingido)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="3f10f-147">Os números máximos de canais de comunicação disponíveis estão em uso.</span><span class="sxs-lookup"><span data-stu-id="3f10f-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="3f10f-148">Outro canal não pode ser iniciado neste momento.</span><span class="sxs-lookup"><span data-stu-id="3f10f-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="3f10f-149"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ incompatibilidade de revisão de erro)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="3f10f-150">Há uma incompatibilidade entre a versão do host e os subsistemas convidados.</span><span class="sxs-lookup"><span data-stu-id="3f10f-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="3f10f-151">Consulte o log de eventos do Windows para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="3f10f-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="3f10f-152"><dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="3f10f-153">A VM não está em execução.</span><span class="sxs-lookup"><span data-stu-id="3f10f-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="3f10f-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f10f-154">Remarks</span></span>

<span data-ttu-id="3f10f-155">A implementação atual dá suporte apenas à interface de pipe nomeado no host e na interface TCP/IP no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="3f10f-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f10f-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f10f-156">Requirements</span></span>



| <span data-ttu-id="3f10f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f10f-157">Requirement</span></span> | <span data-ttu-id="3f10f-158">Valor</span><span class="sxs-lookup"><span data-stu-id="3f10f-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f10f-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f10f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="3f10f-160">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3f10f-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f10f-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f10f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="3f10f-162">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3f10f-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3f10f-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3f10f-163">End of client support</span></span><br/>    | <span data-ttu-id="3f10f-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f10f-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3f10f-165">Produto</span><span class="sxs-lookup"><span data-stu-id="3f10f-165">Product</span></span><br/>                  | <span data-ttu-id="3f10f-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3f10f-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3f10f-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f10f-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f10f-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f10f-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3f10f-169">IID</span><span class="sxs-lookup"><span data-stu-id="3f10f-169">IID</span></span><br/>                      | <span data-ttu-id="3f10f-170">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3f10f-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3f10f-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f10f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f10f-172">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3f10f-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="3f10f-173">**VMEndpointType**</span><span class="sxs-lookup"><span data-stu-id="3f10f-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

