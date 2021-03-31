---
title: Propriedade IVMNetworkAdapter EthernetAddress (VPCCOMInterfaces. h)
description: Endereço Ethernet (MAC) da interface de rede.
ms.assetid: 2d94c5b3-6b69-4fb1-bee4-081dc026dde3
keywords:
- Propriedade EthernetAddress Virtual PC
- Propriedade EthernetAddress Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, Propriedade EthernetAddress
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.EthernetAddress
- IVMNetworkAdapter.get_EthernetAddress
- IVMNetworkAdapter.put_EthernetAddress
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7afb8f9035b0a663e01eeead95dc3f4f6bdec2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644214"
---
# <a name="ivmnetworkadapterethernetaddress-property"></a><span data-ttu-id="74cdc-106">Propriedade IVMNetworkAdapter:: EthernetAddress</span><span class="sxs-lookup"><span data-stu-id="74cdc-106">IVMNetworkAdapter::EthernetAddress property</span></span>

<span data-ttu-id="74cdc-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="74cdc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="74cdc-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="74cdc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="74cdc-109">Recupera e define o endereço Ethernet (MAC) da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="74cdc-109">Retrieves and sets the Ethernet (MAC) address of the network interface.</span></span>

<span data-ttu-id="74cdc-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="74cdc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74cdc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74cdc-111">Syntax</span></span>


```C++
HRESULT put_EthernetAddress(
  [in]          BSTR ethernetAddress
);

HRESULT get_EthernetAddress(
  [out, retval] BSTR *ethernetAddress
);
```



## <a name="property-value"></a><span data-ttu-id="74cdc-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="74cdc-112">Property value</span></span>

<span data-ttu-id="74cdc-113">O endereço MAC da NIC virtual.</span><span class="sxs-lookup"><span data-stu-id="74cdc-113">The MAC address of the virtual NIC.</span></span> <span data-ttu-id="74cdc-114">Ele deve ter o formato "*XX* - *XX* XX XX XX XX -  -  -  - ", em que cada *X* é um dígito hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="74cdc-114">It should have the form "*XX*-*XX*-*XX*-*XX*-*XX*-*XX*" where each *X* is a hexadecimal digit.</span></span>

## <a name="error-codes"></a><span data-ttu-id="74cdc-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="74cdc-115">Error codes</span></span>



| <span data-ttu-id="74cdc-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="74cdc-116">Name/value</span></span>                                                                                                                                                                         | <span data-ttu-id="74cdc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="74cdc-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74cdc-118"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="74cdc-118"><dt>S\_OK</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="74cdc-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="74cdc-119">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="74cdc-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="74cdc-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                              | <span data-ttu-id="74cdc-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="74cdc-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="74cdc-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="74cdc-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                           | <span data-ttu-id="74cdc-123">O parâmetro não está no formato correto.</span><span class="sxs-lookup"><span data-stu-id="74cdc-123">The parameter is not in the correct format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="74cdc-124"><dt>VM \_ E não é possível \_ \_ definir o \_ \_ \_ endereço MAC dinâmico</dt> <dt>0xA004070A</dt></span><span class="sxs-lookup"><span data-stu-id="74cdc-124"><dt>VM\_E\_CANT\_SET\_DYNAMIC\_MAC\_ADDRESS</dt> <dt>0xA004070A</dt></span></span> </dl> | <span data-ttu-id="74cdc-125">O endereço Ethernet para uma interface de rede pode ser gerado dinamicamente ou pode ser definido como um endereço estático pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="74cdc-125">The Ethernet address for a network interface can either be generated dynamically or can be set to a static address by the user.</span></span> <span data-ttu-id="74cdc-126">Este método não pode ser chamado quando o endereço está definido para ser gerado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="74cdc-126">This method cannot be called when the address is set to be generated dynamically.</span></span> <span data-ttu-id="74cdc-127">A propriedade [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) é usada para alterar o comportamento de geração do endereço Ethernet.</span><span class="sxs-lookup"><span data-stu-id="74cdc-127">The [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) property is used to change the generation behavior of the Ethernet address.</span></span><br/> |
| <dl> <span data-ttu-id="74cdc-128"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="74cdc-128"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                      | <span data-ttu-id="74cdc-129">A máquina virtual não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="74cdc-129">The virtual machine was not found.</span></span> <span data-ttu-id="74cdc-130">Isso poderá ocorrer se o computador tiver sido removido após a criação do objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="74cdc-130">This may occur if the machine was removed after the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object was created.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="74cdc-131"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="74cdc-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                      | <span data-ttu-id="74cdc-132">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="74cdc-132">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="74cdc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74cdc-133">Requirements</span></span>



| <span data-ttu-id="74cdc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="74cdc-134">Requirement</span></span> | <span data-ttu-id="74cdc-135">Valor</span><span class="sxs-lookup"><span data-stu-id="74cdc-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74cdc-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74cdc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="74cdc-137">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="74cdc-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74cdc-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74cdc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="74cdc-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="74cdc-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="74cdc-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="74cdc-140">End of client support</span></span><br/>    | <span data-ttu-id="74cdc-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="74cdc-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="74cdc-142">Produto</span><span class="sxs-lookup"><span data-stu-id="74cdc-142">Product</span></span><br/>                  | <span data-ttu-id="74cdc-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="74cdc-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="74cdc-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74cdc-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="74cdc-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="74cdc-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="74cdc-146">IID</span><span class="sxs-lookup"><span data-stu-id="74cdc-146">IID</span></span><br/>                      | <span data-ttu-id="74cdc-147">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="74cdc-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="74cdc-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="74cdc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74cdc-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="74cdc-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

