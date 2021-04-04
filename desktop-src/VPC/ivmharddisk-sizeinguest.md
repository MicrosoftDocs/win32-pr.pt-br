---
title: Propriedade IVMHardDisk SizeInGuest (VPCCOMInterfaces. h)
description: Recupera o tamanho do disco rígido virtual no sistema operacional convidado.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Propriedade SizeInGuest Virtual PC
- Propriedade SizeInGuest Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtual PC, Propriedade SizeInGuest
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
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085968"
---
# <a name="ivmharddisksizeinguest-property"></a>Propriedade IVMHardDisk:: SizeInGuest

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o tamanho do disco rígido virtual no sistema operacional convidado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valor da propriedade

O tamanho, em bytes, da imagem do disco rígido. Esse valor é uma **variante** do tipo VT \_ decimal.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                  |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro é **NULL**.<br/>                                                     |
| <dl> <dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt> </dl> | Não foi possível encontrar o arquivo de disco rígido virtual atual.<br/>                         |
| <dl> <dt>VM \_ 0xA004067C \_ de \_ \_ \_ falha de abertura de imagem de HD</dt> <dt></dt> </dl>                  | Ocorreu um erro ao tentar abrir o arquivo de imagem de disco rígido atual.<br/>   |
| <dl> <dt>VM \_ E & 0xA0040681 de \_ \_ \_ acesso de imagem de HD</dt> <dt></dt> </dl>                      | Ocorreu um erro ao tentar acessar o arquivo de imagem de disco rígido atual.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

