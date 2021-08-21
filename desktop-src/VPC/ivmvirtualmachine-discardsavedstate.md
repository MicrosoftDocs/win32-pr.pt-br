---
title: Método IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Descarta todas as informações de estado salvas de uma máquina virtual salva.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- DiscardSavedState do método virtual PC
- Método DiscardSavedState Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff30406328ae13004505440ae2fb8b18b2e1fdf8ac19dcbfbe77b063e54df688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471976"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a>IVMVirtualMachine: método iscardSavedState de:D

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Descarta todas as informações de estado salvas de uma máquina virtual salva.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                           | Descrição                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                 | A operação foi bem-sucedida.<br/>                               |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>           | A configuração é desconhecida.<br/>                               |
| <dl> <dt>**VM \_ E \_ VM \_ executando**</dt> <dt>0xA0040500</dt> </dl>           | A máquina virtual está em execução.<br/>                             |
| <dl> <dt>**VM \_ E \_ VM \_ não \_ 0xA00400501 \_ estado salvo**</dt> <dt></dt> </dl> | A máquina virtual não está em execução, mas não tem estado salvo.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>           | Ocorreu um erro inesperado.<br/>                           |



 

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

 

