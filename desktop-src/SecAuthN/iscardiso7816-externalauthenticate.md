---
description: Constrói um comando APDU (unidade de dados do protocolo de aplicativo) que atualiza condicionalmente o status de segurança, verificando a identidade do computador quando o cartão inteligente não confia nele.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'Método ISCardISO7816:: ExternalAuthenticate (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370666"
---
# <a name="iscardiso7816externalauthenticate-method"></a>Método ISCardISO7816:: ExternalAuthenticate

\[O método **ExternalAuthenticate** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ExternalAuthenticate** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que atualiza condicionalmente o status de segurança, verificando a identidade do computador quando o [*cartão inteligente*](../secgloss/s-gly.md) não confia nele.

O comando usa o resultado (Sim ou não) do cálculo pelo cartão (com base em um desafio emitido anteriormente pelo cartão, por exemplo, pelo \_ comando ins get \_ Challenge), uma chave (possivelmente segredo) armazenada no cartão e os dados de autenticação transmitidos pelo dispositivo de interface.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byAlgorithmRef* \[ no\]
</dt> <dd>

A referência do algoritmo no cartão.

Se esse valor for zero, isso indica que nenhuma informação é fornecida. A referência do algoritmo é conhecida antes de emitir o comando ou é fornecida no campo de dados.

</dd> <dt>

*bySecretRef* \[ no\]
</dt> <dd>

A referência do segredo.



| Valor                                                                                                                                                                                    | Significado                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nenhuma informação**</dt> </dl>                     | Posição do bit: 00000000<br/> Nenhuma informação é fornecida. A referência do segredo é conhecida antes de emitir o comando ou é fornecida no campo de dados.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Ref global**</dt> </dl>         | Posição do bit: 0-------<br/> Dados de referência global (uma chave específica de MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Referência específica**</dt> </dl> | Posição do bit: 1-------<br/> Dados de referência específicos (uma chave específica de DF).<br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posição do bit:-XX-----<br/> 00 (outros valores são RFU).<br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**RADIUS**</dt> </dl>                         | Posição do bit:---xxxxx<br/> Número do segredo.<br/>                                                                                                             |



 

</dd> <dt>

*pChallenge* \[ no\]
</dt> <dd>

Um ponteiro para os dados relacionados à autenticação. Esse parâmetro pode ser **nulo**.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um parâmetro inválido foi passado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                            |



 

## <a name="remarks"></a>Comentários

Para que o comando encapsulado seja bem-sucedido, o último desafio obtido do cartão deve ser válido.

As comparações malsucedidas podem ser registradas no cartão (por exemplo, para limitar o número de outras tentativas de uso dos dados de referência).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardISO7816**](iscardiso7816.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 é definido como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
