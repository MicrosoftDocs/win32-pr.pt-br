---
description: O método ReadBinary constrói um comando APDU (unidade de dados de protocolo de aplicativo) que adquire uma mensagem de resposta que fornece a parte do conteúdo de um arquivo elementar de forma transparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'Método ISCardISO7816:: ReadBinary (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829753"
---
# <a name="iscardiso7816readbinary-method"></a>Método ISCardISO7816:: ReadBinary

\[O método **ReadBinary** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ReadBinary** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que adquire uma mensagem de resposta que fornece a parte do conteúdo de um arquivo elementar de forma transparente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ no\]
</dt> <dd>

O campo P1-P2, deslocamento para o primeiro byte a ser lido desde o início do arquivo. Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo. Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.

</dd> <dt>

*byP2* \[ no\]
</dt> <dd>

O campo P1-P2, deslocamento para o primeiro byte a ser lido desde o início do arquivo. Se B8 = 1 em P1, a B7 e a B6 de P1 são definidas como zero (RFU bits), B5 a B1 de P1 são um identificador curto de EF e P2 é o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo. Se B8 = 0 em P1, P1 \| \| P2 será o deslocamento do primeiro byte a ser lido em unidades de dados do início do arquivo.

</dd> <dt>

*lBytesToRead* \[ no\]
</dt> <dd>

Número de bytes a serem lidos do EF transparente.

Se o campo Le contiver apenas zeros, dentro do limite de 256 por comprimento curto ou 65536 para comprimento estendido, todos os bytes até o final do arquivo devem ser lidos.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado usando o ponteiro *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

Arquivos elementares sem uma estrutura transparente não podem ser apagados. O comando encapsulado aborta se aplicado a um arquivo elementar sem uma estrutura transparente.

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
