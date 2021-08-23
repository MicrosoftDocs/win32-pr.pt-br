---
title: Método IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces.h)
description: Exclui uma configuração de máquina virtual.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Computador Virtual do método DeleteVirtualMachine
- Computador Virtual do método DeleteVirtualMachine, interface IVMVirtualPC
- INTERFACE IVMVirtualPC Pc Virtual , método DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3471106beeffdfe756ad0793004b68d0a55fd14dda28a9796f4540d2503a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471326"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>Método IVMVirtualPC::D eleteVirtualMachine

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Exclui uma configuração de máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualMachine* \[ Em\]
</dt> <dd>

Um ponteiro para um [**objeto IVMVirtualMachine que**](ivmvirtualmachine.md) representa a configuração da máquina virtual a ser excluída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | Não foi possível encontrar a configuração especificada.<br/>                                      |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                                | O *parâmetro virtualMachine* era **NULL.**<br/>                                         |
| <dl> <dt>**VM \_ E \_ VM \_ EM EXECUÇÃO**</dt> <dt>0xA0040500</dt> </dl>                        | A máquina virtual está em execução.<br/>                                                      |
| <dl> <dt>**VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA**</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentários

Somente máquinas virtuais paradas podem ser excluídas. Observe que qualquer estado salvo existente ou dados de unidade de desfazer para essa configuração serão excluídos além do arquivo de configuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

