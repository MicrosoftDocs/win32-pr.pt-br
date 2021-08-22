---
description: O método UpdateBinary constrói um comando APDU (unidade de dados do protocolo de aplicativo) que atualiza os bits presentes em um arquivo elementar com os bits dados no comando APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: Método ISCardISO7816::UpdateBinary (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46f7bbc66d76fd9d07390e6d78f25cc96111801cea8f715d84b81e704518cbbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577006"
---
# <a name="iscardiso7816updatebinary-method"></a>Método ISCardISO7816::UpdateBinary

\[O **método UpdateBinary** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método UpdateBinary** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo) que atualiza os bits presentes em um arquivo elementar com os bits dados no comando APDU.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdateBinary(
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

Deslocamento para o local de gravação (atualização) no binário do início do binário. Se b8=1 em P1, b7 e b6 de P1 são definidos como zero (bits RFU), b5 a b1 de P1 são um identificador de EF curto e P2 é o deslocamento do primeiro byte a ser atualizado em unidades de dados do início do arquivo. Se b8=0 em P1, P1 P2 será o deslocamento do primeiro byte a ser atualizado em unidades de dados do \| \| início do arquivo.

</dd> <dt>

*byP2* \[ Em\]
</dt> <dd>

Deslocamento para o local de gravação (atualização) no binário do início do binário. Se b8=1 em P1, b7 e b6 de P1 são definidos como zero (bits RFU), b5 a b1 de P1 são um identificador de EF curto e P2 é o deslocamento do primeiro byte a ser atualizado em unidades de dados do início do arquivo. Se b8=0 em P1, P1 P2 será o deslocamento do primeiro byte a ser atualizado em unidades de dados do \| \| início do arquivo.

</dd> <dt>

*pData* \[ Em\]
</dt> <dd>

Ponteiro para a cadeia de caracteres de unidades de dados a serem atualizadas.

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

O comando encapsulado só poderá ser executado se o status de segurança do cartão inteligente satisfaça os atributos de segurança do arquivo elementar que está sendo processado.

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
