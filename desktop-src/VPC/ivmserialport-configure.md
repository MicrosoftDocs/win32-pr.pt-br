---
title: Método de configuração de IVMSerialPort (VPCCOMInterfaces. h)
description: Configura a porta serial.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurar o método virtual PC
- Configurar o método virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, método configure
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009438"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="21be1-106">Método IVMSerialPort:: Configure</span><span class="sxs-lookup"><span data-stu-id="21be1-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="21be1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="21be1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="21be1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="21be1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="21be1-109">Configura a porta serial.</span><span class="sxs-lookup"><span data-stu-id="21be1-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="21be1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21be1-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="21be1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21be1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21be1-112">*PortType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21be1-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21be1-113">O tipo de porta serial.</span><span class="sxs-lookup"><span data-stu-id="21be1-113">The type of serial port.</span></span> <span data-ttu-id="21be1-114">Para obter uma lista de valores, consulte [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="21be1-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="21be1-115">*portaname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21be1-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21be1-116">O nome da porta serial.</span><span class="sxs-lookup"><span data-stu-id="21be1-116">The name of the serial port.</span></span> <span data-ttu-id="21be1-117">Por exemplo, "COM1" para **vmSerialPort \_ HostPort**, "C: \\SerialPort.txt" para **vmSerialPort \_ textfile** ou " \\ \\ *nome_do_servidor* \\ pipe pipeName \\ " para **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="21be1-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="21be1-118">*vmConnectImmediately* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="21be1-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21be1-119">**True** se a porta serial do host precisar ser aberta imediatamente quando a máquina virtual for iniciada; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="21be1-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="21be1-120">Ignorado se *PortType* não for **vmSerialPort \_ HostPort**.</span><span class="sxs-lookup"><span data-stu-id="21be1-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21be1-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21be1-121">Return value</span></span>

<span data-ttu-id="21be1-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="21be1-122">This method can return one of these values.</span></span>



| <span data-ttu-id="21be1-123">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="21be1-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="21be1-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="21be1-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21be1-125"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="21be1-126">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21be1-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="21be1-127"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="21be1-128">O parâmetro *PortType* não é válido.</span><span class="sxs-lookup"><span data-stu-id="21be1-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="21be1-129"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="21be1-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="21be1-130">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="21be1-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="21be1-131"><dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="21be1-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="21be1-132">O parâmetro *PortName* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="21be1-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="21be1-133"><dt>**HRESULT \_ DO \_ Win32 (erro \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="21be1-134">Não há memória suficiente disponível para concluir esta solicitação.</span><span class="sxs-lookup"><span data-stu-id="21be1-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="21be1-135"><dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="21be1-136">O caminho especificado pelo parâmetro *PortName* é muito longo.</span><span class="sxs-lookup"><span data-stu-id="21be1-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="21be1-137">O caminho deve ser menor que **o \_ caminho máximo** (260) caracteres.</span><span class="sxs-lookup"><span data-stu-id="21be1-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="21be1-138"><dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="21be1-139">O parâmetro *PortName* contém um caractere inválido (um de " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="21be1-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="21be1-140"><dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="21be1-141">O parâmetro *PortName* especifica um caminho relativo ou vazio.</span><span class="sxs-lookup"><span data-stu-id="21be1-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="21be1-142">Um caminho absoluto é necessário.</span><span class="sxs-lookup"><span data-stu-id="21be1-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="21be1-143"><dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="21be1-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="21be1-144">A configuração desta máquina virtual não é válida.</span><span class="sxs-lookup"><span data-stu-id="21be1-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="21be1-145"><dt>**VM \_ E \_ pref \_ \_ valor ilegal**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="21be1-146">A porta especificada já está em uso.</span><span class="sxs-lookup"><span data-stu-id="21be1-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="21be1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21be1-147">Requirements</span></span>



| <span data-ttu-id="21be1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="21be1-148">Requirement</span></span> | <span data-ttu-id="21be1-149">Valor</span><span class="sxs-lookup"><span data-stu-id="21be1-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21be1-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21be1-150">Minimum supported client</span></span><br/> | <span data-ttu-id="21be1-151">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="21be1-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21be1-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21be1-152">Minimum supported server</span></span><br/> | <span data-ttu-id="21be1-153">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="21be1-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="21be1-154">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="21be1-154">End of client support</span></span><br/>    | <span data-ttu-id="21be1-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21be1-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="21be1-156">Produto</span><span class="sxs-lookup"><span data-stu-id="21be1-156">Product</span></span><br/>                  | <span data-ttu-id="21be1-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="21be1-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="21be1-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21be1-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="21be1-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="21be1-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="21be1-160">IID</span><span class="sxs-lookup"><span data-stu-id="21be1-160">IID</span></span><br/>                      | <span data-ttu-id="21be1-161">IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="21be1-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="21be1-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="21be1-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21be1-163">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="21be1-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

