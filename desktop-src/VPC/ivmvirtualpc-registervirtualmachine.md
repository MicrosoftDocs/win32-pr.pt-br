---
title: Método IVMVirtualPC RegisterVirtualMachine (VPCCOMInterfaces.h)
description: Registra uma configuração de máquina virtual existente e recupera o objeto da máquina virtual.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Computador Virtual do método RegisterVirtualMachine
- Computador Virtual do método RegisterVirtualMachine, interface IVMVirtualPC
- INTERFACE IVMVirtualPC pc virtual, método RegisterVirtualMachine
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
ms.openlocfilehash: 3752b613bb3adc97d1e0968d989b5c97c616b76883ef89880be7c00d720c62a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998526"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a>Método IVMVirtualPC::RegisterVirtualMachine

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Registra uma configuração de máquina virtual existente e recupera o objeto da máquina virtual.

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

*configurationName* \[ Em\]
</dt> <dd>

O nome da máquina virtual a ser registrada. O comprimento do nome não pode exceder 80 caracteres e o comprimento combinado do nome e caminho não pode exceder **MAX \_ PATH** (260) caracteres. O nome especificado pode conter a extensão .vmc. Se esse parâmetro for **NULL ou** uma cadeia de caracteres vazia, o *parâmetro configurationPath* deverá especificar o caminho completo para o arquivo de configuração.

</dd> <dt>

*configurationPath* \[ Em\]
</dt> <dd>

O caminho para a pasta que contém o arquivo de configuração existente. Se o *parâmetro configurationName* for **NULL ou** uma cadeia de caracteres vazia, isso deverá especificar o caminho completo para o arquivo de configuração existente.

</dd> <dt>

*virtualMachine* \[ out, retval\]
</dt> <dd>

Um ponteiro para um novo [**objeto IVMVirtualMachine**](ivmvirtualmachine.md) que representa essa máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                                                                          |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                    | O *parâmetro configurationName* *ou configurationPath* é inválido ou *virtualMachine* é **NULL.**<br/>                                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0X80070003</dt> </dl> | O sistema não pode encontrar o caminho especificado pelos parâmetros *configurationName* e *configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0X80070002</dt> </dl> | O sistema não pode encontrar o arquivo especificado pelos parâmetros *configurationName* e *configurationPath.*<br/>                                                                                               |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0X8007007B</dt> </dl>    | O *parâmetro configurationPath* contém um caractere inválido (um de " \* ?:<>/ \| "").<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *configurationPath* especifica um caminho vazio ou relativo. Um caminho absoluto é necessário.<br/>                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0X8007006F</dt> </dl> | O caminho especificado pelos parâmetros *configurationName* e *configurationPath* resulta em um caminho muito longo. O comprimento combinado do caminho deve ser menor que **MAX \_ PATH** (260) caracteres.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ \_ ALREADY EXISTS)**</dt> <dt>0X800700B7</dt> </dl>  | Um arquivo de configuração com esse nome já existe nesse local.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ E \_ NOME DA \_ CONFIGURAÇÃO MUITO LONGO \_ \_ 0XA0040401**</dt> <dt></dt> </dl>                | O *parâmetro configurationName* excede 80 caracteres de comprimento.<br/>                                                                                                                                     |
| <dl> <dt>**VM \_ E \_ CONFIG \_ NAME INVALID \_ \_ CHAR**</dt> <dt>0xA0040402</dt> </dl>            | O *parâmetro configurationName* contém um caractere inválido (um de " \* ?:<>/ \| \\ "").<br/>                                                                                                         |
| <dl> <dt>**VM \_ E \_ CONFIG \_ DUPLICATE NAME \_ 0xA0040403**</dt> <dt></dt> </dl>                | Já existe uma máquina virtual com esse nome.<br/>                                                                                                                                                     |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl>     | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/>                                                                                                                   |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Os nomes de máquina virtual não fazem maiúsculas de minúsculas, por exemplo, "MyVM" e "myvm" referem-se à mesma máquina virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

