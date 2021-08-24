---
description: Constrói um comando APDU que inicia uma das operações listadas.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: Método ISCardISO7816::WriteRecord (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a023443f1121759872c4eba0743e5db5b01c8446403b312644e22c83559a527d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014376"
---
# <a name="iscardiso7816writerecord-method"></a>Método ISCardISO7816::WriteRecord

\[O **método WriteRecord** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método WriteRecord** constrói um comando APDU [*(unidade*](../secgloss/a-gly.md) de dados do protocolo de aplicativo) que inicia uma das seguintes operações:

-   A gravação uma vez de um registro.
-   O **OR lógico** dos bytes de dados de um registro já presente no cartão com os bytes de dados do registro determinado no comando APDU.
-   O AND lógico dos bytes de dados de um registro já presente no cartão com os bytes de dados do registro determinado no comando APDU.

Quando nenhuma indicação é dada no byte de codificação de dados, o comportamento OR lógico se aplica.

> [!Note]  
> Ao usar o endereçamento de registro atual, o comando define o ponteiro de registro no registro atualizado com êxito.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byRecordId* \[ Em\]
</dt> <dd>

Identificação de registro. Este é o valor P1:

P1 = '00' designa o registro atual.

P1 != '00' é o número do registro especificado.

</dd> <dt>

*byRefCtrl* \[ Em\]
</dt> <dd>

Codificação do controle de referência P2.



| Valor                                                                                                                                                                                                | Significado                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF atual**</dt> </dl>                     | Posição do bit: 00000---<br/> EF selecionado no momento.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID curta do EF**</dt> </dl>                 | Posição do bit: xxxxx---<br/> Identificador de EF curto.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Primeiro registro**</dt> </dl>             | Posição do bit: -----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Último registro**</dt> </dl>                 | Posição do bit: -----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Próximo Registro**</dt> </dl>                 | Posição do bit: -----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Registro anterior**</dt> </dl> | Posição do bit: -----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Registro \# em P1**</dt> </dl>    | Posição do bit: -----100<br/>                                   |



 

</dd> <dt>

*pData* \[ Em\]
</dt> <dd>

Ponteiro para o registro a ser gravado.

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

O comando encapsulado só poderá ser executado [](../secgloss/s-gly.md) se o status de segurança do cartão inteligente satisfaça os atributos de segurança do arquivo elementar que está sendo processado.

Quando o comando contém um identificador elementar curto válido, ele define o arquivo como arquivo elementar atual. Se outro arquivo elementar estiver selecionado no momento no momento da emissão desse comando, esse comando poderá ser processado sem identificação do arquivo selecionado no momento.

Se o comando encapsulado se aplicar a um arquivo elementar linear fixo ou estruturado cíclico, ele anulará se o comprimento do registro for diferente do comprimento do registro existente. Se ele se aplicar a um arquivo elementar estruturado de variável linear, ele poderá ser executado quando o comprimento do registro for diferente do comprimento do registro existente.

Se P2=xxxxx011 e o arquivo elementar for um arquivo cíclico, esse comando terá o mesmo comportamento que um comando construído usando [**AppendRecord.**](iscardiso7816-appendrecord.md)

Arquivos elementares sem uma estrutura de registro não podem ser gravados. O comando construído será anulado se aplicado a um arquivo elementar sem uma estrutura de registro.

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
