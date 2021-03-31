---
description: Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Método ITabletEventSink:: CursorUp'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171856"
---
# <a name="itableteventsinkcursorup-method"></a>Método ITabletEventSink:: CursorUp

Ocorre quando o usuário dispara a caneta da superfície digitalizadora do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*TCID* \[ no\]
</dt> <dd>

O identificador do Tablet.

</dd> <dt>

*CID* \[ em\]
</dt> <dd>

O identificador da caneta.

</dd> <dt>

*nSerialNumber* \[ no\]
</dt> <dd>

O número de série da caneta.

</dd> <dt>

*cbPkt* \[ no\]
</dt> <dd>

O número de bytes em um pacote de dados da caneta.

</dd> <dt>

*pbPkt* \[ no\]
</dt> <dd>

Os dados da caneta que indicam o local em que a caneta foi levantada do Tablet.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




