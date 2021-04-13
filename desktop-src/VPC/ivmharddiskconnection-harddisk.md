---
title: Propriedade IVMHardDiskConnection HD (VPCCOMInterfaces. h)
description: Recupera um objeto de disco rígido correspondente a esta conexão.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Propriedade HD Virtual PC
- Propriedade HD Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, Propriedade HD
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369716"
---
# <a name="ivmharddiskconnectionharddisk-property"></a><span data-ttu-id="4c770-106">Propriedade IVMHardDiskConnection:: HD</span><span class="sxs-lookup"><span data-stu-id="4c770-106">IVMHardDiskConnection::HardDisk property</span></span>

<span data-ttu-id="4c770-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c770-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c770-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c770-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c770-109">Recupera um objeto de disco rígido correspondente a esta conexão.</span><span class="sxs-lookup"><span data-stu-id="4c770-109">Retrieves a hard disk object corresponding to this connection.</span></span>

<span data-ttu-id="4c770-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4c770-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c770-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c770-111">Syntax</span></span>


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="4c770-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c770-112">Property value</span></span>

<span data-ttu-id="4c770-113">Um objeto [**IVMHardDisk**](ivmharddisk.md) que descreve o disco rígido associado a essa conexão.</span><span class="sxs-lookup"><span data-stu-id="4c770-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4c770-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4c770-114">Error codes</span></span>



| <span data-ttu-id="4c770-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4c770-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="4c770-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4c770-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c770-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4c770-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="4c770-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4c770-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="4c770-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4c770-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="4c770-120">O parâmetro é **nulo** ou não é válido.</span><span class="sxs-lookup"><span data-stu-id="4c770-120">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="4c770-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4c770-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="4c770-122">A configuração atual da máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="4c770-122">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="4c770-123"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4c770-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="4c770-124">O local do barramento desta conexão não foi inicializado corretamente ou o dispositivo neste local não é um disco rígido válido.</span><span class="sxs-lookup"><span data-stu-id="4c770-124">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |
| <dl> <span data-ttu-id="4c770-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4c770-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="4c770-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4c770-126">An unexpected error has occurred.</span></span><br/>                                                                                                |



## <a name="requirements"></a><span data-ttu-id="4c770-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c770-127">Requirements</span></span>



| <span data-ttu-id="4c770-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c770-128">Requirement</span></span> | <span data-ttu-id="4c770-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4c770-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c770-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c770-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c770-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4c770-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c770-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c770-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c770-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c770-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c770-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4c770-134">End of client support</span></span><br/>    | <span data-ttu-id="4c770-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c770-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c770-136">Produto</span><span class="sxs-lookup"><span data-stu-id="4c770-136">Product</span></span><br/>                  | <span data-ttu-id="4c770-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c770-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c770-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c770-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c770-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c770-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c770-140">IID</span><span class="sxs-lookup"><span data-stu-id="4c770-140">IID</span></span><br/>                      | <span data-ttu-id="4c770-141">IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="4c770-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="4c770-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c770-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c770-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="4c770-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

