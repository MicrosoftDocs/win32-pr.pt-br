---
title: Método IvMGuestOS GetOsVersionInfo (VPCCOMInterfaces.h)
description: Recupera informações de versão para o sistema operacional convidado em execução na máquina virtual.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Pc Virtual do método GetOsVersionInfo
- Computador Virtual do método GetOsVersionInfo, interface IVMGuestOS
- INTERFACE IVMGuestOS Pc Virtual, método GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef39259b429d096246bbdbe5cb23e6021f498b2d9d47cd14fb12409eca814c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653466"
---
# <a name="ivmguestosgetosversioninfo-method"></a>Método IVMGuestOS::GetOsVersionInfo

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera informações de versão para o sistema operacional convidado em execução na VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guestOsVersionInfo* \[ out, retval\]
</dt> <dd>

Um ponteiro para uma [**estrutura GUESTOSVERSIONINFOEX.**](guestosversioninfoex.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                       | Descrição                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | A operação foi bem-sucedida.<br/>                                  |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                               | O parâmetro é **NULL.**<br/>                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | Não há memória suficiente disponível para concluir essa solicitação.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                       | Ocorreu um erro inesperado.<br/>                              |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>                  | A VM não está em execução.<br/>                                         |
| <dl> <dt>**VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ ESTÁ**</dt> <dt>0XA0040505</dt> </dl>    | Os componentes de integração não estão instalados nessa VM.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

