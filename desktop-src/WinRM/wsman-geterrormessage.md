---
title: Método WSMan. GetErrorMessage (WSManDisp. h)
description: Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método GetErrorMessage
- Método GetErrorMessage Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, Método GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295787"
---
# <a name="wsmangeterrormessage-method"></a>Método WSMan. GetErrorMessage

Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro. Esse método executa a mesma operação que o WinRM da linha de comando **WinRM** **helpmsg** *decimal ou o número de erro hexadecimal*.

## <a name="syntax"></a>Sintaxe


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*errorNumber* \[ no\]
</dt> <dd>

Um número de mensagem de erro em decimal ou hexadecimal do WinRM, do WinHTTP ou de outros componentes do sistema operacional.

</dd> <dt>

*ErrorMessage* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres de mensagem de erro formatada como mensagens retornadas do comando **WinRM** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O método C++ correspondente é [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





