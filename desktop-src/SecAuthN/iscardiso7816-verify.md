---
description: Constrói um comando APDU (unidade de dados do protocolo de aplicativo) que inicia a comparação (no cartão) dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão (por exemplo, senha).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'Método ISCardISO7816:: Verify (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0d01fe47133ddeaf7bba32a91711d76783bdfbb0a28762d7ddb7f9054d0108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014436"
---
# <a name="iscardiso7816verify-method"></a>Método ISCardISO7816:: Verify

\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Verify** constrói um comando APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) que inicia a comparação (no cartão) dos dados de verificação enviados do dispositivo de interface com os dados de referência armazenados no cartão (por exemplo, senha).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byRefCtrl* \[ no\]
</dt> <dd>

Um quantificador dos dados de referência. A codificação do controle de referência P2 segue.

Quando o corpo estiver vazio, o comando poderá ser usado para recuperar o número ' X ' de novas tentativas permitidas (SW1-SW2 = 63CX) ou para verificar se a verificação não é necessária (SW1-SW2 = 9000).



| Valor                                                                                                                                                                                    | Significado                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nenhuma informação**</dt> </dl>                     | Posição do bit: 00000000<br/> P2 = 00 é reservado para indicar que nenhum qualificador específico é usado nesses cartões em que o comando VERIFY referencia os dados secretos de forma inequívoca.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Ref global**</dt> </dl>         | Posição do bit: 0-------<br/> Um exemplo de ref global seria uma senha.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Referência específica**</dt> </dl> | Posição do bit: 1-------<br/> Um exemplo de ref específica é uma senha específica de DF.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posição do bit:-XX-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Dados de referência \#**</dt> </dl>        | Posição do bit:---xxxxx<br/> O número de dados de referência pode ser, por exemplo, um número de senha ou um identificador curto do EF.<br/>                                                           |



 

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Um ponteiro para os dados de verificação. Este parâmetro pode ser **NULL**. O valor padrão é **NULL**.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com sucesso.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um parâmetro que não é válido foi usado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                          |



 

## <a name="remarks"></a>Comentários

O status de segurança pode ser modificado como resultado de uma comparação. As comparações malsucedidas podem ser registradas no cartão (por exemplo, para limitar o número de outras tentativas de uso dos dados de referência).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
