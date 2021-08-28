---
title: Método de redefinição de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Redefine a máquina virtual.
ms.assetid: 44daf6be-66ce-4291-a535-c30369eed60f
keywords:
- Redefinir o método virtual PC
- Método Reset Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, redefinir método
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Reset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d09204afba2d5c9340350a1fad256e84f8fbf8899c544c7b52d36dfb872c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056774"
---
# <a name="ivmvirtualmachinereset-method"></a>Método IVMVirtualMachine:: Reset

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Redefine a VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reset(
  [out, retval] IVMTask **resetTask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*resetTask* \[ out, retval\]
</dt> <dd>

Um objeto [**IVMTask**](ivmtask.md) que é usado para acompanhar o progresso de conclusão da sequência de redefinição da VM.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                          | Descrição                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | A operação foi bem-sucedida.<br/>                                     |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                  | O parâmetro é **NULL**.<br/>                                        |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt> </dl> | O chamador deve ter permissões de acesso de execução para redefinir esta VM.<br/> |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                     | A VM não está em execução.<br/>                                            |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                          | A configuração é desconhecida.<br/>                                     |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                          | Ocorreu um erro inesperado.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

