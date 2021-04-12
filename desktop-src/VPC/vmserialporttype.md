---
title: Enumeração VMSerialPortType (VPCCOMInterfaces. h)
description: Especifica o tipo de porta serial.
ms.assetid: 1385292b-ee3c-41f0-805a-df126f33cabb
keywords:
- VMSerialPortType de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMSerialPortType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9b6171053e980f1f5dbdc52ef28deed177edba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499572"
---
# <a name="vmserialporttype-enumeration"></a><span data-ttu-id="ccc83-104">Enumeração VMSerialPortType</span><span class="sxs-lookup"><span data-stu-id="ccc83-104">VMSerialPortType enumeration</span></span>

<span data-ttu-id="ccc83-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ccc83-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ccc83-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ccc83-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ccc83-107">Especifica o tipo de porta serial.</span><span class="sxs-lookup"><span data-stu-id="ccc83-107">Specifies the type of serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccc83-108">Syntax</span></span>


```C++
typedef enum  { 
  vmSerialPort_HostPort   = 0,
  vmSerialPort_TextFile   = 1,
  vmSerialPort_NamedPipe  = 2,
  vmSerialPort_Null       = 3
} VMSerialPortType;
```



## <a name="constants"></a><span data-ttu-id="ccc83-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ccc83-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ccc83-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort \_ HostPort**</span><span class="sxs-lookup"><span data-stu-id="ccc83-110"><span id="vmSerialPort_HostPort"></span><span id="vmserialport_hostport"></span><span id="VMSERIALPORT_HOSTPORT"></span>**vmSerialPort\_HostPort**</span></span>
</dt> <dd>

<span data-ttu-id="ccc83-111">Uma porta serial do host.</span><span class="sxs-lookup"><span data-stu-id="ccc83-111">A host serial port.</span></span>

</dd> <dt>

<span data-ttu-id="ccc83-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort \_ textfile**</span><span class="sxs-lookup"><span data-stu-id="ccc83-112"><span id="vmSerialPort_TextFile"></span><span id="vmserialport_textfile"></span><span id="VMSERIALPORT_TEXTFILE"></span>**vmSerialPort\_TextFile**</span></span>
</dt> <dd>

<span data-ttu-id="ccc83-113">Um arquivo de texto de host.</span><span class="sxs-lookup"><span data-stu-id="ccc83-113">A host text file.</span></span>

</dd> <dt>

<span data-ttu-id="ccc83-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort \_ NamedPipe**</span><span class="sxs-lookup"><span data-stu-id="ccc83-114"><span id="vmSerialPort_NamedPipe"></span><span id="vmserialport_namedpipe"></span><span id="VMSERIALPORT_NAMEDPIPE"></span>**vmSerialPort\_NamedPipe**</span></span>
</dt> <dd>

<span data-ttu-id="ccc83-115">Um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="ccc83-115">A named pipe.</span></span>

</dd> <dt>

<span data-ttu-id="ccc83-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort \_ nulo**</span><span class="sxs-lookup"><span data-stu-id="ccc83-116"><span id="vmSerialPort_Null"></span><span id="vmserialport_null"></span><span id="VMSERIALPORT_NULL"></span>**vmSerialPort\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="ccc83-117">Uma porta serial **nula** (descarta todos os bits enviados a ela).</span><span class="sxs-lookup"><span data-stu-id="ccc83-117">A **NULL** serial port (discards all bits sent to it).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccc83-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc83-118">Requirements</span></span>



| <span data-ttu-id="ccc83-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc83-119">Requirement</span></span> | <span data-ttu-id="ccc83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ccc83-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc83-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccc83-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc83-122">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ccc83-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccc83-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccc83-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc83-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ccc83-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ccc83-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ccc83-125">End of client support</span></span><br/>    | <span data-ttu-id="ccc83-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccc83-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ccc83-127">Produto</span><span class="sxs-lookup"><span data-stu-id="ccc83-127">Product</span></span><br/>                  | <span data-ttu-id="ccc83-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ccc83-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ccc83-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccc83-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc83-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc83-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc83-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccc83-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc83-132">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="ccc83-132">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

