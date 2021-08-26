---
description: O método FindCard pesquisa o cartão inteligente e abre uma conexão válida com ele.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: Método ISCardLocate::FindCard (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a0db06f9dcafd211f628eb7cd0be9ed2f800b6f1b980d8e2320cd82b2849d386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014236"
---
# <a name="iscardlocatefindcard-method"></a>Método ISCardLocate::FindCard

\[O **método FindCard** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método FindCard** pesquisa o [*cartão inteligente*](../secgloss/s-gly.md) e abre uma conexão válida com ele.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ShareMode* \[ Em\]
</dt> <dd>

Modo no qual compartilhar ou não compartilhar o cartão inteligente quando uma conexão é aberta a ele.



| Valor                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exclusivo**</dt> </dl> | Ninguém mais usa essa conexão com o cartão inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Compartilhado**</dt> </dl>          | Outros aplicativos podem usar essa conexão.<br/>        |



 

</dd> <dt>

*Protocolos* \[ Em\]
</dt> <dd>

Protocolo a ser usado ao se conectar ao cartão.

T0

T1

RAW

T0 \| T1

</dd> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Especifica quando a [*interface do usuário*](../secgloss/u-gly.md) é exibida:



| Valor                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <dt>**INTERFACE DO USUÁRIO MÍNIMA do SC \_ DLG \_ \_**</dt> </dl> | Exibe a caixa de diálogo somente se o cartão que está sendo pesquisado pelo aplicativo de chamada não estiver localizado e disponível para uso em um leitor. Isso permite que o cartão seja encontrado, conectado (por meio de um mecanismo de caixa de diálogo interno ou usando as funções de retorno de chamada do usuário) e retornado ao aplicativo de chamada.<br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <dt>**SC \_ DLG \_ NO \_ UI**</dt> </dl>                | Não causa nenhuma exibição da interface do usuário, independentemente do resultado da pesquisa.<br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <dt>**INTERFACE DO USUÁRIO DO SC \_ DLG \_ FORCE \_**</dt> </dl>       | Causa a exibição da interface do usuário, independentemente do resultado da pesquisa.<br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*ppCardInfo* \[ out\]
</dt> <dd>

Ponteiro para um ponteiro para uma estrutura de dados que contém ou retorna informações sobre o [*cartão inteligente aberto,*](../secgloss/s-gly.md)se bem-sucedido. Será **NULL se** a operação tiver falhado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                        |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado em *ppCardInfo.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                            |



 

## <a name="remarks"></a>Comentários

Para definir os critérios de pesquisa da pesquisa, chame [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para especificar os nomes de cartão de um cartão inteligente.

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardLocate**](iscardlocate.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardLocate é definido como \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[**ISCardLocate**](iscardlocate.md)
</dt> </dl>

 

 
