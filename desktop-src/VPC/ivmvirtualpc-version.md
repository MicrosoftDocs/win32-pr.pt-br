---
title: Propriedade de versão IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera a versão desta instância do Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propriedade de versão Virtual PC
- Propriedade de versão Virtual PC, interface IVMVirtualPC
- Virtual PC de interface IVMVirtualPC, Propriedade Version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc84fd714c50c0a0adb3084603aeea2419d3ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455981"
---
# <a name="ivmvirtualpcversion-property"></a>Propriedade IVMVirtualPC:: Version

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a versão desta instância do Windows Virtual PC.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a>Valor da propriedade

A versão.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro é **NULL**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



## <a name="remarks"></a>Comentários

As informações de versão do Windows Virtual PC são retornadas como um valor de cadeia de caracteres com o seguinte formato: "*v*. *s*. *BBB*. " *t*", em que *v* é o número de versão principal, *s* é o número de versão secundário, *BBB* é o número de Build, *t* é o tipo de compilação (0 = Build de versão) e o *EE* é a Server Edition (se = Standard Edition, EE = Enterprise Edition).

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

 

