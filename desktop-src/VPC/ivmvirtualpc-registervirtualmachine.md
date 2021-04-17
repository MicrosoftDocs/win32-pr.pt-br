---
title: Método IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces. h)
description: Registra uma configuração de máquina virtual existente e recupera o objeto de máquina virtual.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine do método virtual PC
- Método RegisterVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método RegisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761171"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>Método IVMVirtualPC:: RegisterVirtualMachine

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Registra uma configuração de máquina virtual existente e recupera o objeto de máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ConfigurationName* \[ no\]
</dt> <dd>

O nome da máquina virtual a ser registrada. O comprimento do nome não pode exceder 80 caracteres e o comprimento combinado do nome e do caminho não pode exceder os caracteres do **\_ caminho máximo** (260). O nome especificado pode conter a extensão. vmc. Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, o parâmetro *configurationPath* deverá especificar o caminho completo para o arquivo de configuração.

</dd> <dt>

*configurationPath* \[ no\]
</dt> <dd>

O caminho para a pasta que contém o arquivo de configuração existente. Se o parâmetro *ConfigurationName* for **nulo** ou uma cadeia de caracteres vazia, isso deverá especificar o caminho completo para o arquivo de configuração existente.

</dd> <dt>

*VirtualMachine* \[ out, retval\]
</dt> <dd>

Um ponteiro para um novo objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *ConfigurationName* ou *configurationPath* é inválido ou *VirtualMachine* é **nulo**.<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelos parâmetros *ConfigurationName* e *configurationPath* .<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt> </dl> | O sistema não pode localizar o arquivo especificado pelos parâmetros *ConfigurationName* e *configurationPath* .<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)**</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *configurationPath* contém um caractere inválido (um de " \* ?: <>/ \| " ").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *configurationPath* do parâmetro especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelos parâmetros *ConfigurationName* e *configurationPath* resulta em um caminho muito longo. O comprimento combinado do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (o erro \_ já \_ existe)**</dt> <dt>0x800700b7</dt> </dl>  | Já existe um arquivo de configuração com este nome neste local.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ O \_ nome da configuração E é \_ \_ muito \_ longo**</dt> <dt>0xA0040401</dt> </dl>                | O parâmetro *ConfigurationName* excede 80 caracteres de comprimento.<br/>                                                                                                                                     |
| <dl> <dt>**VM \_ Nome de config & 0xA0040402 de \_ \_ \_ \_ caracteres inválido**</dt> <dt></dt> </dl>            | O parâmetro *ConfigurationName* contém um caractere inválido (um de " \* ?: <>/ \| \\ " ").<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ config \_ \_ nome duplicado**</dt> <dt>0xA0040403</dt> </dl>                | Já existe uma máquina virtual com esse nome.<br/>                                                                                                                                                     |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

