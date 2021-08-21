---
description: Constrói um comando APDU (unidade de dados de protocolo de aplicativo) que define sequencialmente parte do conteúdo de um arquivo elementar para seu estado lógico apagado, começando com um determinado deslocamento.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: Método ISCardISO7816::EraseBinary (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007894"
---
# <a name="iscardiso7816erasebinary-method"></a>Método ISCardISO7816::EraseBinary

\[O **método EraseBinary** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método EraseBinary** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo) que define sequencialmente parte do conteúdo de um arquivo elementar para seu estado lógico apagado, começando com um determinado deslocamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ Em\]
</dt> <dd>

Posição da RFU.

Se b8=1 em P1, b7 e b6 de P1 são definidos como zero (bits RFU), b5 a b1 de P1 são um identificador de EF curto e P2 é o deslocamento do primeiro byte a ser apagado (em unidades de dados) do início do arquivo.

Se b8=0 em P1, P1 P2 será o deslocamento do primeiro byte a ser apagado (em unidades de dados) do início \| \| do arquivo.

Se o campo de dados estiver presente, ele codifica o deslocamento da primeira unidade de dados para não ser apagado. Esse deslocamento deve ser maior do que aquele codificado em P1-P2. Quando o campo de dados está vazio, o comando apaga até o final do arquivo.

</dd> <dt>

*byP2* \[ Em\]
</dt> <dd>

Posição da RFU.

Se b8=1 em P1, b7 e b6 de P1 são definidos como zero (bits RFU), b5 a b1 de P1 são um identificador de EF curto e P2 é o deslocamento do primeiro byte a ser apagado (em unidades de dados) do início do arquivo.

Se b8=0 em P1, P1 P2 será o deslocamento do primeiro byte a ser apagado (em unidades de dados) do início \| \| do arquivo.

Se o campo de dados estiver presente, ele codifica o deslocamento da primeira unidade de dados para não ser apagado. Esse deslocamento deve ser maior do que aquele codificado em P1-P2. Quando o campo de dados está vazio, o comando apaga até o final do arquivo.

</dd> <dt>

*pData* \[ Em\]
</dt> <dd>

Um ponteiro para os dados que especificam o intervalo de apagas. Esse parâmetro pode ser **NULL.**

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **NULL.**

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido [](../secgloss/s-gly.md) como **NULL,** um objeto [**ISCardCmd**](iscardcmd.md) de cartão inteligente é criado internamente e retornado usando o *ponteiro ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | A operação foi concluída com sucesso.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um parâmetro que não é válido foi passado.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                            |



 

## <a name="remarks"></a>Comentários

O comando encapsulado só poderá ser executado [](../secgloss/s-gly.md) se o status de segurança do cartão inteligente satisfaça os atributos de segurança do arquivo elementar que está sendo processado.

Quando o comando contém um identificador elementar curto válido, ele define o arquivo como arquivo elementar atual.

Arquivos elementares sem uma estrutura transparente não podem ser apagados. O comando encapsulado será anulado se aplicado a um arquivo elementar sem uma estrutura transparente.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
