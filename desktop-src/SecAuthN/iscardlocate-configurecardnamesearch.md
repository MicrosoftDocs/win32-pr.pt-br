---
description: O método ConfigureCardNameSearch especifica os nomes de cartão a serem usados na pesquisa do cartão inteligente.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Método ISCardLocate:: ConfigureCardNameSearch (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170022"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a>Método ISCardLocate:: ConfigureCardNameSearch

\[O método **ConfigureCardNameSearch** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **ConfigureCardNameSearch** especifica os nomes de cartão a serem usados na pesquisa do [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCardNames* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz segura de automação de nomes de cartão na forma BSTR.

</dd> <dt>

*pGroupNames* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz segura de automação de nomes de grupos de cartões/leitores no formato BSTR para adicionar à pesquisa.

</dd> <dt>

*bstrTitle* \[ no\]
</dt> <dd>

Título da caixa de diálogo para o controle comum de pesquisa.

</dd> <dt>

*lFlags* \[ no\]
</dt> <dd>

Especifica quando a [*interface do usuário*](../secgloss/u-gly.md) é exibida.



| Valor                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**\_ \_ IU mínima SC \_ Dlg**</dt> </dl> | Exibe a caixa de diálogo somente se o cartão que está sendo pesquisado pelo aplicativo de chamada não estiver localizado e disponível para uso em um leitor. Isso permite que o cartão seja encontrado, conectado (por meio de um mecanismo de caixa de diálogo interno ou usando as funções de retorno de chamada do usuário) e retornado ao aplicativo de chamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ sem \_ interface do usuário**</dt> </dl>                | Não faz nenhuma exibição da interface do usuário, independentemente do resultado da pesquisa.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**\_IU de \_ força \_ do SC Dlg**</dt> </dl>       | Faz com que a interface do usuário seja exibida, independentemente do resultado da pesquisa.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                                         |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *pCardNames* ou *pGroupNames*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                             |



 

## <a name="remarks"></a>Comentários

Para localizar o [*cartão inteligente*](../secgloss/s-gly.md), chame [**FindCard**](iscardlocate-findcard.md).

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardLocate**](iscardlocate.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardLocate é definido como 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FindCard**](iscardlocate-findcard.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
