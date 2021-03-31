---
description: O método selectfile constrói um comando APDU (unidade de dados do protocolo de aplicativo) que define um arquivo elementar atual em um canal lógico. Os comandos subsequentes podem se referir implicitamente ao arquivo atual por meio do canal lógico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'Método ISCardISO7816:: selectfile (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169699"
---
# <a name="iscardiso7816selectfile-method"></a>Método ISCardISO7816:: selectfile

\[O método **selectfile** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **selectfile** constrói um comando APDU ( [*unidade de dados do protocolo de aplicativo*](../secgloss/a-gly.md) ) que define um arquivo elementar atual em um canal lógico. Os comandos subsequentes podem se referir implicitamente ao arquivo atual por meio do canal lógico.

Selecionar um diretório (DF) dentro do repositório filestore — que pode ser a raiz (MF) do filestore — o torna o DF atual. Após essa seleção, um arquivo elementar atual implícito pode ser referenciado por meio desse canal lógico.

Selecionar um arquivo elementar define o arquivo selecionado e seu pai como arquivos atuais.

Após a resposta a ser redefinida, o MF é selecionado implicitamente por meio do canal lógico básico, a menos que especificado de forma diferente nos bytes históricos ou na cadeia de caracteres de dados inicial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*byP1* \[ no\]
</dt> <dd>

Controle de seleção.



| P1 (byte superior no Word): 8 7 6 5 4 3 2 1                                                                                                                                                            | Significado                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | Selecionar ID do arquivo<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF ou MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | DF filho<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF em DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | DF pai do DF atual<br/> |



 

Quando P1 = 00, o cartão saberá devido a uma codificação específica da ID do arquivo ou devido ao contexto de execução do comando se o arquivo a ser selecionado for o MF, um DF ou um EF.

Quando P1-P2 = 0000, se uma ID de arquivo for fornecida, ela deverá ser exclusiva nos seguintes ambientes:

-   Filhos imediatos da DF atual
-   DF pai
-   Filhos imediatos da DF pai

Se P1-P2 = 0000 e se o campo de dados estiver vazio ou for igual a 3F00, selecione o MF.

Quando P1 = 04, o campo de dados é um nome de DF, possivelmente truncado à direita.

Quando há suporte, os comandos sucessivos com o mesmo campo de dados devem selecionar o DFs cujos nomes correspondem ao campo de dados (ou seja, começar com o campo de dados de comando). Se o cartão aceitar o comando com um campo de dados vazio, todos ou um subconjunto do DFs poderá ser selecionado sucessivamente.

</dd> <dt>

*byP2* \[ no\]
</dt> <dd>

Controle de seleção.

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Dados para a operação, se necessário; Senão, **NULL**. Os tipos de dados que são passados nesse parâmetro incluem:

-   ID do arquivo
-   caminho do MF
-   caminho do DF atual
-   Nome da DF

</dd> <dt>

*lBytesToRead* \[ no\]
</dt> <dd>

Empty (ou seja, 0) ou o comprimento máximo dos dados esperados em resposta.

</dd> <dt>

*ppCmd* \[ entrada, saída\]
</dt> <dd>

Na entrada, um ponteiro para um objeto de interface [**ISCardCmd**](iscardcmd.md) ou **nulo**.

No retorno, ele é preenchido com o comando APDU construído por essa operação. Se *ppCmd* foi definido como **NULL**, um objeto [**ISCardCmd**](iscardcmd.md) de [*cartão inteligente*](../secgloss/s-gly.md) será criado internamente e retornado por meio do ponteiro *ppCmd* .

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

A menos que especificado de outra forma, a execução correta do comando encapsulado modifica o status de segurança de acordo com as seguintes regras:

-   Quando o arquivo elementar atual é alterado ou quando não há nenhum arquivo elementar atual, o status de segurança específico para um antigo arquivo elements atual é perdido.
-   Quando o diretório de repositório de pasta atual (DF) é descendente ou é idêntico ao DF atual anterior, o status de segurança específico do DF atual antigo é perdido. O status de segurança comum a todos os ancestrais comuns do DF atual e novo é mantido.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
