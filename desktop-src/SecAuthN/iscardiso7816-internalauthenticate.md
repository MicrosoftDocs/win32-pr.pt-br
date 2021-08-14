---
description: Constrói um comando APDU (unidade de dados do protocolo de aplicativo) que inicia o cálculo dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante (por exemplo, uma chave) armazenados no cartão.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: Método ISCardISO7816::InternalAuthenticate (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d4c3385313fb5b9c9c7ba72957244bd81757b0cd1e79bcec906e740c69b66292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922986"
---
# <a name="iscardiso7816internalauthenticate-method"></a>Método ISCardISO7816::InternalAuthenticate

\[O **método InternalAuthenticate** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método InternalAuthenticate** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo) que inicia o cálculo dos dados de autenticação pelo cartão usando os dados de desafio enviados do dispositivo de interface e um segredo relevante (por exemplo, uma chave) armazenados no cartão.

Quando o segredo relevante é anexado ao MF, o comando pode ser usado para autenticar o cartão como um todo.

Quando o segredo relevante é anexado a outro DF, o comando pode ser usado para autenticar esse DF.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byAlgorithmRef* \[ Em\]
</dt> <dd>

Referência do algoritmo no cartão.

Se esse valor for zero, isso indicará que nenhuma informação é dada. A referência do algoritmo é conhecida antes de emissão do comando ou é fornecida no campo de dados.

</dd> <dt>

*bySecretRef* \[ Em\]
</dt> <dd>

Referência do segredo.



| Valor                                                                                                                                                                                    | Significado                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Sem informações**</dt> </dl>                     | Posição do bit: 00000000 <br/> Nenhuma informação é dada. A referência do segredo é conhecida antes de emissão do comando ou é fornecida no campo de dados.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Referência global**</dt> </dl>         | Posição do bit: 0------- <br/> Dados de referência global (uma chave específica do MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Ref específico**</dt> </dl> | Posição do bit: 1-------<br/> Dados de referência específicos (uma chave específica do DF).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Posição do bit: -xx-----<br/> 00 (outros valores são RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Segredo**</dt> </dl>                         | Posição do bit: ---xxxxx<br/> Número do segredo.<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[ Em\]
</dt> <dd>

Ponteiro para os dados relacionados à autenticação (por exemplo, desafio).

</dd> <dt>

*lReplyBytes* \[ Em\]
</dt> <dd>

Número máximo de bytes esperados em resposta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **NULL.**

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd tiver* sido [](../secgloss/s-gly.md) definido como **NULL,** um objeto [**ISCardCmd**](iscardcmd.md) de cartão inteligente será criado internamente e retornado usando o *ponteiro ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

A execução bem-sucedida do comando pode estar sujeita à conclusão bem-sucedida de comandos anteriores (por exemplo, VERIFY ou SELECT FILE) ou seleções (por exemplo, o segredo relevante).

Se uma chave e um algoritmo forem selecionados no momento durante a emissão do comando, o comando poderá usar implicitamente a chave e o algoritmo.

O número de vezes que o comando é emitido pode ser registrado no cartão para limitar o número de tentativas de usar o segredo relevante ou o algoritmo.

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
