---
title: Propriedade IVMHardDiskConnection UndoHardDisk (VPCCOMInterfaces. h)
description: Recupera um objeto de disco rígido correspondente à imagem de desfazer disco da conexão.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- Propriedade UndoHardDisk Virtual PC
- Propriedade UndoHardDisk Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, Propriedade UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085133"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="45edb-106">Propriedade IVMHardDiskConnection:: UndoHardDisk</span><span class="sxs-lookup"><span data-stu-id="45edb-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="45edb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45edb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="45edb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="45edb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="45edb-109">Recupera um objeto de disco rígido correspondente à imagem de desfazer disco da conexão.</span><span class="sxs-lookup"><span data-stu-id="45edb-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="45edb-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="45edb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45edb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45edb-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="45edb-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="45edb-112">Property value</span></span>

<span data-ttu-id="45edb-113">Um objeto [**IVMHardDisk**](ivmharddisk.md) que descreve o disco rígido de desfazer associado a essa conexão.</span><span class="sxs-lookup"><span data-stu-id="45edb-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45edb-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="45edb-114">Error codes</span></span>



| <span data-ttu-id="45edb-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="45edb-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="45edb-116">Significado</span><span class="sxs-lookup"><span data-stu-id="45edb-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45edb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="45edb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="45edb-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="45edb-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="45edb-119"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="45edb-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="45edb-120">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="45edb-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="45edb-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="45edb-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="45edb-122">O parâmetro é **nulo** ou não é válido.</span><span class="sxs-lookup"><span data-stu-id="45edb-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="45edb-123"><dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="45edb-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="45edb-124">O disco de desfazer para esta conexão não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="45edb-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="45edb-125"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="45edb-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="45edb-126">A configuração atual da máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="45edb-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="45edb-127"><dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="45edb-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="45edb-128">O local do barramento desta conexão não foi inicializado corretamente ou o dispositivo neste local não é um disco rígido válido.</span><span class="sxs-lookup"><span data-stu-id="45edb-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="45edb-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45edb-129">Requirements</span></span>



| <span data-ttu-id="45edb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="45edb-130">Requirement</span></span> | <span data-ttu-id="45edb-131">Valor</span><span class="sxs-lookup"><span data-stu-id="45edb-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45edb-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45edb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="45edb-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="45edb-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45edb-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45edb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="45edb-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="45edb-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="45edb-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="45edb-136">End of client support</span></span><br/>    | <span data-ttu-id="45edb-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45edb-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="45edb-138">Produto</span><span class="sxs-lookup"><span data-stu-id="45edb-138">Product</span></span><br/>                  | <span data-ttu-id="45edb-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="45edb-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="45edb-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45edb-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="45edb-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="45edb-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="45edb-142">IID</span><span class="sxs-lookup"><span data-stu-id="45edb-142">IID</span></span><br/>                      | <span data-ttu-id="45edb-143">IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="45edb-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="45edb-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="45edb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45edb-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="45edb-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

