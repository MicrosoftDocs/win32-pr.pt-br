---
description: O método GetData constrói um comando APDU (unidade de dados do protocolo de aplicativo) que recupera um único objeto de dados primitivo ou um conjunto de objetos de dados (contidos em um objeto de dados construído), dependendo do tipo de arquivo selecionado.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: Método ISCardISO7816::GetData (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ef783092edb87a29203c83afcf67fb594eb84dcc296621379c9f39a9ccbcc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672376"
---
# <a name="iscardiso7816getdata-method"></a>Método ISCardISO7816::GetData

\[O **método GetData** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método GetData** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados de protocolo de aplicativo) que recupera um único objeto de dados primitivo ou um conjunto de objetos de dados (contidos em um objeto de dados construído), dependendo do tipo de arquivo selecionado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ Em\]
</dt> <dd>

Parâmetros.



| Valor                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 – 00FF</dt> </dl> | Marca BER-TLV (1 byte) em P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Dados do aplicativo (codificação proprietária)<br/> |
| <dl> <dt>0200 – 02FF</dt> </dl> | Marca SIMPLE-TLV em P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Marca BER-TLV (2 bytes) em P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ Em\]
</dt> <dd>

Parâmetros.



| Valor                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 – 00FF</dt> </dl> | Marca BER-TLV (1 byte) em P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Dados do aplicativo (codificação proprietária)<br/> |
| <dl> <dt>0200 – 02FF</dt> </dl> | Marca SIMPLE-TLV em P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Marca BER-TLV (2 bytes) em P1-P2<br/>        |



 

</dd> <dt>

*lBytesToGet* \[ Em\]
</dt> <dd>

Número de bytes esperados na resposta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **NULL.**

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd tiver* sido [](../secgloss/s-gly.md) definido como **NULL,** um objeto [**ISCardCmd**](iscardcmd.md) de cartão inteligente será criado internamente e retornado usando o *ponteiro ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

O comando encapsulado só poderá ser executado [](../secgloss/s-gly.md) se o status de segurança do cartão inteligente satisfaça os atributos de segurança do arquivo elementar que está sendo lido. As condições de segurança dependem da política do cartão e podem ser manipuladas por meio de [**ExternalAuthenticate,**](iscardiso7816-externalauthenticate.md) [**InternalAuthenticate,**](iscardiso7816-internalauthenticate.md) [**ISCardAuth**](iscardauth.md)e assim por diante.

Para selecionar um arquivo, chame [**SelectFile.**](iscardiso7816-selectfile.md)

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**PutData**](iscardiso7816-putdata.md)
</dt> <dt>

[**SelectFile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
