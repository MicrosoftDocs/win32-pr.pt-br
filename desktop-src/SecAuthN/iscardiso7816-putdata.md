---
description: O método PutData constrói um comando APDU (unidade de dados de protocolo de aplicativo) que armazena um único objeto de dados primitivos ou o conjunto de objetos de dados contidos em um objeto de dados construído, dependendo do arquivo selecionado.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: 'ISCardISO7816: método utData de:P (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829328"
---
# <a name="iscardiso7816putdata-method"></a>ISCardISO7816: método utData de:P

\[O método **PutData** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **PutData** constrói um comando APDU ( [*unidade de dados de protocolo de aplicativo*](../secgloss/a-gly.md) ) que armazena um único objeto de dados primitivos ou o conjunto de objetos de dados contidos em um objeto de dados construído, dependendo do arquivo selecionado.

A forma como os objetos são armazenados (gravar uma vez e/ou atualizar e/ou acrescentar) depende da definição ou da natureza dos objetos de dados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PutData(
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

Codificação de P1-P2.



| Valor                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | BER – marca TLV (1 byte) em P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Dados de aplicativo (codificação proprietária)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Marca de TLV simples em P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV marca (2 bytes) em P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ no\]
</dt> <dd>

Codificação de P1-P2.



| Valor                                                                                  | Significado                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000-003F</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0040-00FF</dt> </dl> | BER – marca TLV (1 byte) em P2<br/>            |
| <dl> <dt>0100-01FF</dt> </dl> | Dados de aplicativo (codificação proprietária)<br/> |
| <dl> <dt>0200-02FF</dt> </dl> | Marca de TLV simples em P2<br/>                  |
| <dl> <dt>0300-03FF</dt> </dl> | RFU<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | BER-TLV marca (2 bytes) em P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Ponteiro para um buffer de bytes que contém os parâmetros e os dados a serem gravados.

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

O comando só poderá ser executado se o status de segurança satisfizer as condições de segurança definidas pelo aplicativo no [*contexto*](../secgloss/c-gly.md) para a função.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Armazenar dados de aplicativos
</dt> <dd>

Quando o valor P1-P2 está no intervalo de 0100 a 01FF, o valor de P1-P2 deve ser um identificador reservado para testes internos de cartão e para serviços proprietários significativos em um determinado contexto de aplicativo.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Armazenar objetos de dados
</dt> <dd>

Quando o valor P1-P2 está no intervalo de 0040 a 00FF, o valor de P2 deve ser uma marca BER-TLV em um único byte. O valor de 00FF é reservado para indicar que o campo de dados transporta objetos de dados BER-TLV.

Quando o valor de P1-P2 está no intervalo de 0200 a 02FF, o valor de P2 deve ser uma marca de TLV simples. O valor 0200 é RFU. O valor 02FF é reservado para indicar que o campo de dados contém objetos de dados de TLV simples.

Quando o valor de P1-P2 estiver no intervalo de 4000 a FFFF, o valor de P1-P2 deverá ser uma marca BER-TLV em dois bytes. Os valores de 4000 a FFFF são RFU.

Quando um objeto de dados primitivo é fornecido, o campo de dados da mensagem de comando deve conter o valor do objeto de dados primitivo correspondente.

Quando um objeto de dados construído é fornecido, o campo de dados da mensagem de comando deve conter o valor do objeto de dados construído (ou seja, objetos de dados incluindo sua marca, comprimento e valor).

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
