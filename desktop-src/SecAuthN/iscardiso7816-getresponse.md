---
description: O método GetResponse constrói um comando APDU (unidade de dados do protocolo de aplicativo) que transmite comandos APDU (ou parte de um comando APDU) que, caso contrário, não poderiam ser transmitidos pelos protocolos disponíveis.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: Método ISCardISO7816::GetResponse (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 21646b7de844509b28bb0ea437fa76cd9fa835932333677f919872daecb3ce60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481144"
---
# <a name="iscardiso7816getresponse-method"></a>Método ISCardISO7816::GetResponse

\[O **método GetResponse** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método GetResponse** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo) que transmite comandos APDU (ou parte de um comando APDU) que, caso contrário, não poderiam ser transmitidos pelos protocolos disponíveis.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ Em\]
</dt> <dd>

De acordo com a ISO 7816-4, P1 deve ser zero (RFU).

</dd> <dt>

*byP2* \[ Em\]
</dt> <dd>

De acordo com a ISO 7816-4, P2 deve ser zero (RFU).

</dd> <dt>

*lDataLength* \[ Em\]
</dt> <dd>

Comprimento dos dados transmitidos.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **NULL.**

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd foi* definido [](../secgloss/s-gly.md) como **NULL,** um objeto [**ISCardCmd**](iscardcmd.md) de cartão inteligente é criado internamente e retornado por meio do *ponteiro ppCmd.*

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

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
