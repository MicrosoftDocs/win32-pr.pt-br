---
description: O método ManageChannel constrói um comando APDU (unidade de dados de protocolo de aplicativo) que abre e fecha canais lógicos.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'Método ISCardISO7816:: ManageChannel (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92fb91c0630996938e247dbc244ac0c311c52531401367d5326bd197ffaabf9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481105"
---
# <a name="iscardiso7816managechannel-method"></a>Método ISCardISO7816:: ManageChannel

\[O método **ManageChannel** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ManageChannel** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que abre e fecha canais lógicos.

A função abrir abre um novo canal lógico diferente do básico. As opções são fornecidas para o cartão atribuir um número de canal lógico ou para o número de canal lógico a ser fornecido ao cartão.

A função close fecha explicitamente um canal lógico diferente do básico. Após o fechamento bem-sucedido, o canal lógico deverá estar disponível para reutilização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byChannelState* \[ no\]
</dt> <dd>

O bit B8 de P1 é usado para indicar a função Open ou a função close; se B8 for 0, o canal de gerenciamento deverá abrir um canal lógico e, se B8 for 1, o canal de gerenciamento deverá fechar um canal lógico:

P1 = ' 00 ' para abrir

P1 = ' 80 ' para fechar

Outros valores são RFU

</dd> <dt>

*byChannel* \[ no\]
</dt> <dd>

Para a função Open (P1 = ' 00 '), os bits B1 e B2 de P2 são usados para codificar o número de canal lógico da mesma maneira que no byte de classe, os outros bits de P2 são RFU.

Quando B1 e B2 de P2 forem **nulas**, o cartão atribuirá um número de canal lógico que será retornado em bits B1 e B2 do campo de dados.

Quando B1 e/ou B2 de P2 não são **nulas**, eles codificam um número de canal lógico diferente do básico; em seguida, o cartão abrirá o número de canal lógico atribuído externamente.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Quando a função Open for executada com êxito a partir do canal lógico básico, o MF deverá ser selecionado implicitamente como o DF atual e o status de segurança do novo canal lógico deverá ser o mesmo que o canal lógico básico após a ATR. O status de segurança do novo canal lógico deve ser separado do de qualquer outro canal lógico.

Quando a função Open é executada com êxito de um canal lógico, que não é o básico, o DF atual do canal lógico que emitiu o comando será selecionado como o DF atual. Além disso, o status de segurança para o novo canal lógico deve ser o mesmo que o status de segurança do canal lógico do qual a função abrir foi executada.

Após uma função de fechamento bem-sucedida, o status de segurança relacionado a esse canal lógico é perdido.

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
