---
title: Mensagem de LB_DIR (WinUser. h)
description: Adiciona nomes à lista exibida por uma caixa de listagem. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. \_O diretório lb também pode adicionar letras de unidade mapeadas à caixa de listagem.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- controles de Windows de mensagem de LB_DIR
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3add3c0ea14c637e0240ab296095bcc720aff9efb4c3e8e99a2f3de7019a711
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671662"
---
# <a name="lb_dir-message"></a>Mensagem de dir. LB \_

Adiciona nomes à lista exibida por uma caixa de listagem. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. **Lb \_ DIR** também pode adicionar letras de unidade mapeadas à caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Os atributos dos arquivos ou diretórios a serem adicionados à caixa de listagem. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_arquivo DDL**</dt> </dl>       | Inclui arquivos arquivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_diretório DDL**</dt> </dl> | Inclui subdiretórios. Os nomes de subdiretórios são colocados entre colchetes ( \[ \] ).<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unidades DDL**</dt> </dl>          | Todas as unidades mapeadas são adicionadas à lista. As unidades são listadas no formato \[ - *x* - \] , em que *x* é a letra da unidade.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**exclusivo de DDL \_**</dt> </dl> | Inclui somente arquivos com os atributos especificados. Por padrão, os arquivos de leitura/gravação são listados mesmo que o DDL \_ ReadWrite não seja especificado.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ oculto**</dt> </dl>          | Inclui arquivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**\_somente leitura DDL**</dt> </dl>    | Inclui arquivos somente leitura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**ReadWrite de DDL \_**</dt> </dl> | Inclui arquivos de leitura/gravação sem atributos adicionais. Essa é a configuração padrão.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Inclui arquivos do sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que especifica um caminho absoluto, um caminho relativo ou um nome de arquivo. Um caminho absoluto pode começar com uma letra da unidade (por exemplo, d: \) ou um nome UNC (por exemplo, \\ \\ *MachineName* \\ *ShareName*).

Se a cadeia de caracteres especificar um nome de arquivo ou diretório que tenha os atributos especificados pelo parâmetro *wParam* , o nome do arquivo ou diretório será adicionado à lista. Se o nome de arquivo ou diretório contiver caracteres curinga (? ou \* ), todos os arquivos ou diretórios que correspondem à expressão curinga e têm os atributos especificados pelo parâmetro *wParam* são adicionados à lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, o valor de retorno será o índice de base zero do sobrenome adicionado à lista.

Se ocorrer um erro, o valor de retorno será um erro de LB \_ . Se não houver espaço suficiente para armazenar as novas cadeias de caracteres, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens de **\_ dir de lb** subsequentes tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

Se *wParam* incluir o \_ sinalizador de diretório DDL e *lParam* especificar todos os subdiretórios de um diretório de primeiro nível, como C: \\ temp \\ \* , a caixa de listagem sempre incluirá uma entrada ".." para o diretório raiz. Isso é verdadeiro mesmo que o diretório raiz tenha atributos ocultos ou de sistema e os \_ sinalizadores de sistema ocultos e DDL DDL \_ não sejam especificados. O diretório raiz de um volume NTFS tem atributos ocultos e de sistema.

A lista exibe nomes de FileName longos, se houver.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP. Isso pode causar problemas. por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode em japonês Windows ficarão confusos. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





