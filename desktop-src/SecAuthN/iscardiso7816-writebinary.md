---
description: O método WriteBinary constrói um comando APDU (unidade de dados de protocolo de aplicativo) que grava valores binários em um arquivo elementar.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'Método ISCardISO7816:: WriteBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 198a8eedc38636f60886af251c8520ef4726f362958c13a25fc3bf32653d7c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922915"
---
# <a name="iscardiso7816writebinary-method"></a>Método ISCardISO7816:: WriteBinary

\[O método **WriteBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **WriteBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que grava valores binários em um arquivo elementar.

Dependendo dos atributos do arquivo, o comando executa uma das seguintes operações:

-   A lógica ou os bits já presentes no cartão com os bits fornecidos no comando APDU (o estado de apagamento lógico dos bits do arquivo é 0).
-   A lógica e o dos bits já estão presentes no cartão com os bits fornecidos no comando APDU (o estado de apagamento lógico dos bits do arquivo é 1).
-   A gravação única no cartão dos bits fornecidos no comando APDU.

Quando nenhuma indicação é fornecida no byte de codificação de dados, a lógica ou o comportamento se aplica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ no\]
</dt> <dd>

Offset para o local de gravação desde o início do arquivo binário (EF). Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser gravado em unidades de dados do início do arquivo. Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser gravado em unidades de dados desde o início do arquivo.

</dd> <dt>

*byP2* \[ no\]
</dt> <dd>

Offset para o local de gravação desde o início do arquivo binário (EF). Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser gravado em unidades de dados do início do arquivo. Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser gravado em unidades de dados desde o início do arquivo.

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Ponteiro para a cadeia de caracteres das unidades de dados a serem gravadas.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .

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

O comando encapsulado só poderá ser executado se o status de segurança do [*cartão inteligente*](../secgloss/s-gly.md) satisfizer os atributos de segurança do arquivo elementar que está sendo processado.

Quando o comando contém um identificador elementar curto válido, ele define o arquivo como o arquivo elementar atual.

Quando uma operação de gravação binária tiver sido aplicada a uma unidade de dados de um EF de gravação única, qualquer outra operação de gravação referente a essa unidade de dados será anulada se o conteúdo da unidade de dados ou o indicador de estado de apagamento lógico (se houver) anexado a essa unidade de dados for diferente do estado de apagamento lógico.

Os arquivos elementares sem uma estrutura transparente não podem ser gravados. O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
