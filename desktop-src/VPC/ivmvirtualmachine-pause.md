---
title: Método IVMVirtualMachine PAUSE (VPCCOMInterfaces. h)
description: Pausa a máquina virtual.
ms.assetid: 29ac40c4-7713-4782-8a31-42f2c32b8f7d
keywords:
- Pausar o método virtual PC
- Pausar método virtual PC, interface IVMVirtualMachine
- Virtual PC de interface IVMVirtualMachine, método pause
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Pause
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bbab3da710a66c1e737e02693cb2002452ec11154b1be3da0e3568fea38e59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471476"
---
# <a name="ivmvirtualmachinepause-method"></a>IVMVirtualMachine: método ause de:P

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Pausa a VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                          | Descrição                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | A operação foi bem-sucedida.<br/>                                     |
| <dl> <dt>**E \_ FALHA**</dt> <dt>0x80004005</dt> </dl>                                     | A VM já está pausada.<br/>                                         |
| <dl> <dt>**HRESULT \_ DO \_ Win32 (erro de \_ acesso \_ negado)**</dt> <dt>0x80070005</dt> </dl> | O chamador deve ter permissões de acesso de execução para pausar essa VM.<br/> |
| <dl> <dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt> </dl>                           | A operação não foi concluída oportunamente.<br/>                |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>                     | A máquina virtual não está em execução.<br/>                               |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                          | A configuração é desconhecida.<br/>                                     |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                          | Ocorreu um erro inesperado.<br/>                                 |



 

## <a name="remarks"></a>Comentários

**Pause** não salva o estado atual da VM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

