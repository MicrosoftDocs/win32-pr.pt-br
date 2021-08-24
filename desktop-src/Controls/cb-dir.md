---
title: Mensagem de CB_DIR (WinUser. h)
description: Adiciona nomes à lista exibida pela caixa de combinação. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. \_O diretório CB também pode adicionar letras de unidade mapeadas à lista.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- controles de Windows de mensagem de CB_DIR
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: defa19ffdebfb448e1a89c141da0b275c1df1bffdcfa9e3914293400d706b7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577116"
---
# <a name="cb_dir-message"></a>\_Mensagem de diretório CB

Adiciona nomes à lista exibida pela caixa de combinação. A mensagem adiciona os nomes de diretórios e arquivos que correspondem a uma cadeia de caracteres especificada e um conjunto de atributos de arquivo. **CB \_ DIR** também pode adicionar letras de unidade mapeadas à lista.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Os atributos dos arquivos ou diretórios a serem adicionados à caixa de combinação. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**\_arquivo DDL**</dt> </dl>       | Inclui arquivos arquivados.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_diretório DDL**</dt> </dl> | Inclui subdiretórios, que são colocados entre colchetes ( \[ \] ).<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_unidades DDL**</dt> </dl>          | Todas as unidades mapeadas são adicionadas à lista. As unidades são listadas no formato \[ - *x* - \] , em que *x* é a letra da unidade.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**exclusivo de DDL \_**</dt> </dl> | Inclui somente arquivos com os atributos especificados. Por padrão, os arquivos de leitura/gravação são listados mesmo que o DDL \_ ReadWrite não seja especificado.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ oculto**</dt> </dl>          | Inclui arquivos ocultos.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**\_somente leitura DDL**</dt> </dl>    | Inclui arquivos somente leitura.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**ReadWrite de DDL \_**</dt> </dl> | Inclui arquivos de leitura/gravação sem atributos adicionais. Esse é o padrão.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_sistema DDL**</dt> </dl>          | Inclui arquivos do sistema.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro **LPCTSTR** para uma cadeia de caracteres terminada em nulo que especifica um caminho absoluto, um caminho relativo ou um nome de arquivo. Um caminho absoluto pode começar com uma letra da unidade (por exemplo, d: \) ou um nome UNC (por exemplo, \\ \\ *MachineName* \\ *ShareName*). Se a cadeia de caracteres especificar um nome de arquivo ou diretório que tenha os atributos especificados pelo parâmetro *wParam* , o nome do arquivo ou diretório será adicionado à lista. Se o nome do arquivo ou o nome do diretório contiver caracteres curinga (? ou \* ), todos os arquivos ou diretórios que correspondem à expressão curinga e têm os atributos especificados pelo parâmetro *wParam* são adicionados à lista exibida na caixa de combinação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, o valor de retorno será o índice de base zero do sobrenome adicionado à lista.

Se ocorrer um erro, o valor de retorno será CB \_ Err. Se não houver espaço suficiente para armazenar as novas cadeias de caracteres, o valor de retorno será CB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

Se *wParam* incluir o \_ sinalizador de diretório DDL e *lParam* especificar todos os subdiretórios de um diretório de primeiro nível, como C: \\ temp \\ \* , a caixa de listagem sempre incluirá uma entrada ".." para o diretório raiz. Isso é verdadeiro mesmo que o diretório raiz tenha atributos ocultos ou de sistema e os \_ sinalizadores de sistema ocultos e DDL DDL \_ não sejam especificados. O diretório raiz de um volume NTFS tem atributos ocultos e de sistema.

A lista exibe nomes de arquivo longos, se houver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**inserção de CB \_**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





