---
title: Propriedade IVMHardDisk SizeInGuest (VPCCOMInterfaces.h)
description: Recupera o tamanho do disco rígido virtual no sistema operacional convidado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Propriedade SizeInGuest Pc Virtual
- Propriedade SizeInGuest Virtual PC , interface IVMHardDisk
- INTERFACE IVMHardDisk Pc Virtual , propriedade SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efbdcf9f5aa60a8dfdce9c71de745e0567995b90df13ffd39b5969689de099c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653286"
---
# <a name="ivmharddisksizeinguest-property"></a>Propriedade IVMHardDisk::SizeInGuest

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tamanho do disco rígido virtual no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor da propriedade

O tamanho, em bytes, da imagem do disco rígido. Esse valor é uma **VARIANT do** tipo VT \_ DECIMAL.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                  |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                    | O parâmetro é **NULL.**<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | Não foi possível encontrar o arquivo de disco rígido virtual atual.<br/>                         |
| <dl> <dt>VM \_ O \_ E HD IMAGE OPEN FALHA \_ \_ \_ 0XA004067C</dt> <dt></dt> </dl>                  | Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.<br/>   |
| <dl> <dt>VM \_ E \_ HD \_ IMAGE \_ ACCESS</dt> <dt>0xA0040681</dt> </dl>                      | Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ocorreu um erro inesperado.<br/>                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHardDisk é definido como \_ ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

