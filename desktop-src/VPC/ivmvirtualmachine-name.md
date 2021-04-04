---
title: Propriedade nome do IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nome da configuração da máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propriedade do nome Virtual PC
- Propriedade de nome Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade Name
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
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085696"
---
# <a name="ivmvirtualmachinename-property"></a>Propriedade IVMVirtualMachine:: Name

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o nome da configuração da máquina virtual.

Esta propriedade é de leitura/gravação.

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

Especifica o nome da configuração da máquina virtual. O comprimento do nome não pode ter mais de 80 caracteres e o comprimento total do caminho totalmente qualificado que inclui o arquivo de configuração de nome da máquina virtual não pode ser maior que o máximo de caracteres de **\_ caminho** (260).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                    | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                       | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                         | O parâmetro é **NULL**.<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | O parâmetro não é válido ou é uma cadeia de caracteres vazia.<br/>                                    |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>                 | A configuração é desconhecida.<br/>                                                        |
| <dl> <dt>VM \_ E \_ pref \_ VM \_ ativa</dt> <dt>0xA0040302</dt> </dl>            | A máquina virtual está em execução ou salva.<br/>                                             |
| <dl> <dt>VM \_ E \_ config \_ sem \_ nome</dt> <dt>0xA0040400</dt> </dl>            | O parâmetro *virtualMachineName* está vazio.<br/>                                         |
| <dl> <dt>VM \_ O \_ nome da configuração E é \_ \_ muito \_ longo</dt> <dt>0xA00400401</dt> </dl>    | O parâmetro contém muitos caracteres.<br/>                                          |
| <dl> <dt>VM \_ Nome de config & 0xA0040402 de \_ \_ \_ \_ caracteres inválido</dt> <dt></dt> </dl> | O parâmetro contém um dos seguintes caracteres inválidos " \* ?: <>/ \| \\ " ".<br/> |
| <dl> <dt>VM \_ E \_ config \_ \_ nome duplicado</dt> <dt>0xA0040403</dt> </dl>     | O nome especificado já existe como o nome de outra máquina virtual.<br/>            |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                 | Ocorreu um erro inesperado.<br/>                                                    |



## <a name="remarks"></a>Comentários

Os nomes de máquina virtual não diferenciam maiúsculas de minúsculas, por exemplo, "MyVM" e "MyVM" referem-se à mesma máquina virtual. Essa é a propriedade padrão para [**IVMVirtualMachine**](ivmvirtualmachine.md).

Se VPC.exe estiver em execução e a VM for salva, a definição da propriedade **Name** não terá sucesso. Se VPC.exe não estiver em execução e a VM for salva, a configuração da propriedade **nome** terá sucesso quando VPC.exe for iniciado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

