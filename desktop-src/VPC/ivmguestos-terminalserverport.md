---
title: Propriedade IVMGuestOS TerminalServerPort
description: Porta usada por Serviços de Área de Trabalho Remota no sistema operacional convidado.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Propriedade TerminalServerPort Virtual PC
- Propriedade TerminalServerPort Virtual PC, interface IVMGuestOS
- IVMGuestOS interface virtual PC, Propriedade TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086268"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="f9a6a-106">Propriedade IVMGuestOS:: TerminalServerPort</span><span class="sxs-lookup"><span data-stu-id="f9a6a-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="f9a6a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f9a6a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f9a6a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f9a6a-109">Porta usada pelo Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="f9a6a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a6a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9a6a-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="f9a6a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f9a6a-112">Property value</span></span>

<span data-ttu-id="f9a6a-113">Retorna a porta usada por Serviços de Área de Trabalho Remota no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="f9a6a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f9a6a-114">Value</span></span>                                                                              | <span data-ttu-id="f9a6a-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f9a6a-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f9a6a-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="f9a6a-117">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="f9a6a-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="f9a6a-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="f9a6a-119">Intervalo válido</span><span class="sxs-lookup"><span data-stu-id="f9a6a-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="f9a6a-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="f9a6a-121">O valor de porta válido não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="f9a6a-122">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f9a6a-122">Error codes</span></span>



| <span data-ttu-id="f9a6a-123">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="f9a6a-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f9a6a-124">Significado</span><span class="sxs-lookup"><span data-stu-id="f9a6a-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9a6a-125"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f9a6a-126">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="f9a6a-127"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="f9a6a-128">O Serviços de Área de Trabalho Remota ainda não foi inicializado no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="f9a6a-129"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="f9a6a-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="f9a6a-130">O parâmetro *tsPort* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f9a6a-131"><dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f9a6a-132">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f9a6a-133"><dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f9a6a-134">Os componentes de integração não estão instalados nesta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="f9a6a-135"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="f9a6a-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f9a6a-136">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="f9a6a-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9a6a-137">Remarks</span></span>

<span data-ttu-id="f9a6a-138">O valor dessa propriedade não é válido, a menos que a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) seja **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="f9a6a-139">Se a propriedade [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) for **Variant \_ false** devido a um erro de conexão na porta, o valor retornado pela propriedade **TerminalServerPort** conterá o valor de erro.</span><span class="sxs-lookup"><span data-stu-id="f9a6a-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a6a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9a6a-140">Requirements</span></span>



| <span data-ttu-id="f9a6a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a6a-141">Requirement</span></span> | <span data-ttu-id="f9a6a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="f9a6a-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a6a-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9a6a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a6a-144">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9a6a-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9a6a-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9a6a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a6a-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f9a6a-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f9a6a-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f9a6a-147">End of client support</span></span><br/>    | <span data-ttu-id="f9a6a-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9a6a-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="f9a6a-149">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9a6a-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9a6a-150"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9a6a-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="f9a6a-151">IID</span><span class="sxs-lookup"><span data-stu-id="f9a6a-151">IID</span></span><br/>                      | <span data-ttu-id="f9a6a-152">IID \_ IVMGuestOS é definido como 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f9a6a-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f9a6a-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9a6a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a6a-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="f9a6a-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

