---
title: Propriedade IVMVirtualMachine Name (VPCCOMInterfaces.h)
description: Nome da configuração da máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propriedade Name Pc Virtual
- Propriedade name Pc Virtual , interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , propriedade Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219e6fcb24805feb0370bd157d014767a9348e87e500d8c94fa26ff502b6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006796"
---
# <a name="ivmvirtualmachinename-property"></a>Propriedade IVMVirtualMachine::Name

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o nome da configuração da máquina virtual.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o nome da configuração da máquina virtual. O comprimento do nome não pode ter mais de 80 caracteres e o comprimento total do caminho totalmente qualificado que inclui o arquivo de configuração de nome da máquina virtual não pode ser maior que **MAX \_ PATH** (260) caracteres.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                    | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                         | O parâmetro é **NULL.**<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | O parâmetro não é válido ou é uma cadeia de caracteres vazia.<br/>                                    |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                 | A configuração é desconhecida.<br/>                                                        |
| <dl> <dt>VM \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl>            | A máquina virtual está em execução ou salva.<br/>                                             |
| <dl> <dt>VM \_ E \_ CONFIG \_ NO NAME \_ 0XA0040400</dt> <dt></dt> </dl>            | O *parâmetro virtualMachineName* está vazio.<br/>                                         |
| <dl> <dt>VM \_ E \_ NOME DE \_ CONFIGURAÇÃO MUITO LONGO \_ \_ 0XA00400401</dt> <dt></dt> </dl>    | O parâmetro contém muitos caracteres.<br/>                                          |
| <dl> <dt>VM \_ E \_ CONFIG \_ NAME INVALID \_ \_ CHAR</dt> <dt>0xA0040402</dt> </dl> | O parâmetro contém um dos seguintes caracteres inválidos " \* ?:<>/ \| \\ "".<br/> |
| <dl> <dt>VM \_ E \_ CONFIG \_ DUPLICATE NAME \_ 0xA0040403</dt> <dt></dt> </dl>     | O nome especificado já existe como o nome de outra máquina virtual.<br/>            |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                 | Ocorreu um erro inesperado.<br/>                                                    |



## <a name="remarks"></a>Comentários

Os nomes de máquina virtual não são sensíveis a maiúsculas e minúsculas, por exemplo, "MyVM" e "myvm" referem-se à mesma máquina virtual. Essa é a propriedade padrão para [**IVMVirtualMachine.**](ivmvirtualmachine.md)

Se VPC.exe estiver em execução e a VM for salva, a configuração **da propriedade Nome** não terá êxito. Se VPC.exe estiver em execução e a VM for salva, a definição da propriedade **Nome** terá êxito quando VPC.exe for iniciado em seguida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

