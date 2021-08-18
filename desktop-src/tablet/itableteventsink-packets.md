---
description: Ocorre quando a caneta está se movendo no digitalizador.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: Método ITabletEventSink::P ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 29b118771fb5217ed13c01ef9376ad9b426e1ecd74a4bf931d8412a0b47e913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712116"
---
# <a name="itableteventsinkpackets-method"></a>Método ITabletEventSink::P ackets

Ocorre quando a caneta está se movendo no digitalizador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tcid* \[ Em\]
</dt> <dd>

O identificador do tablet.

</dd> <dt>

*cPkts* \[ Em\]
</dt> <dd>

O número de pacotes.

</dd> <dt>

*cbPkts* \[ Em\]
</dt> <dd>

O tamanho do buffer de pacote

</dd> <dt>

*pbPkts* \[ Em\]
</dt> <dd>

O buffer de pacote.

</dd> <dt>

*pnSerialNumbers* \[ Em\]
</dt> <dd>

A matriz de número de série.

</dd> <dt>

*Cid* 
</dt> <dd>

O identificador da caneta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletEventSink Interface**](itableteventsink.md)
</dt> </dl>

 

 




