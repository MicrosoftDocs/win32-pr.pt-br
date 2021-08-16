---
description: Contém informações sobre a caixa de diálogo exibida pela função CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: CRYPTUI_SELECTCERTIFICATE_STRUCT estrutura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f8cc80f740e26ac2d067705c9aac9aee387b91e28cb057366587375c874ae0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768230"
---
# <a name="cryptui_selectcertificate_struct-structure"></a>Estrutura \_ STRUCT CRYPTUI SELECTCERTIFICATE \_

A **estrutura \_ \_ STRUCT CRYPTUI SELECTCERTIFICATE** contém informações sobre a caixa de diálogo exibida pela [**função CryptUIDlgSelectCertificate.**](cryptuidlgselectcertificate.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwsize**
</dt> <dd>

O tamanho, em bytes, dessa estrutura.

</dd> <dt>

**Hwndparent**
</dt> <dd>

O alça da janela pai da caixa de diálogo. Se esse valor for **NULL,** a janela pai será a janela da área de trabalho padrão.

</dd> <dt>

**dwFlags**
</dt> <dd>

Especifica opções adicionais para a [**função CryptUIDlgSelectCertificate.**](cryptuidlgselectcertificate.md) Isso pode ser zero ou um **OR** bit a bit dos valores a seguir.



| Valor                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt> </dl>                              | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ LEGACY**</dt> </dl>                                       | Especifica que a caixa de diálogo herdada deve ser exibida.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ MULTISELECT**</dt> </dl>                        | Permite que o usuário selecione mais de um certificado na caixa de diálogo. Se esse sinalizador for definido, a [**função CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) sempre retornará **NULL.** O **membro hSelectedCertStore** dessa estrutura deve conter um handle para um repositório de certificados. Os certificados selecionados pelo usuário serão adicionados a esse armazenamento.<br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <dt>**CRYPTUI \_ SELECTCERT \_ COLOCAR JANELA MAIS \_ \_ ALTO**</dt> </dl> | Força a interface do usuário de criptografia a ser a janela superior na tela.<br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

**szTitle**
</dt> <dd>

O título de exibição da caixa de diálogo. Se o valor desse membro for **NULL,** o título padrão de "Selecionar Certificado" será usado.

</dd> <dt>

**dwDontUseColumn**
</dt> <dd>

Sinalizadores que podem ser combinados para excluir colunas da exibição.



| Valor                                                                                                                                                                                                                                                                                       | Significado                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ ISSUEDTO \_ COLUMN**</dt> <dt>1 (0X1)</dt> </dl>             | Não exibir informações **ISSUEDTO.**<br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ ISSUEDBY \_ COLUMN**</dt> <dt>2 (0X2)</dt> </dl>             | Não exibir informações **ISSUEDBY.**<br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ INTENDEDUSE \_ COLUMN**</dt> <dt>4 (0X4)</dt> </dl>    | Não exibir informações **de IntendedUse.**<br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ FRIENDLYNAME \_ COLUMN**</dt> <dt>8 (0X8)</dt> </dl> | Não exibir informações de nome.<br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ LOCATION \_ COLUMN**</dt> <dt>16 (0x10)</dt> </dl>           | Não exibir informações de localização.<br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <dt>**CRYPTUI \_ SELECT \_ EXPIRATION \_ COLUMN**</dt> <dt>32 (0X20)</dt> </dl>     | Não exibir informações de expiração.<br/>      |



 

</dd> <dt>

**szDisplayString**
</dt> <dd>

Texto exibido na caixa de diálogo para instruir o usuário. Se o valor desse membro for **NULL,** a cadeia de caracteres padrão "Selecionar um certificado que você deseja usar" será usada.

</dd> <dt>

**pFilterCallback**
</dt> <dd>

Um ponteiro para uma função de retorno de chamada [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) que filtra os certificados exibidos na caixa de diálogo.

</dd> <dt>

**pDisplayCallback**
</dt> <dd>

Um ponteiro para uma função de retorno de chamada [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) que exibe certificados que o usuário seleciona para exibir.

</dd> <dt>

**pvCallbackData**
</dt> <dd>

Dados adicionais que são passados para as funções de retorno de chamada especificadas pelos membros **pFilterCallback** e **pDisplayCallback.**

</dd> <dt>

**cDisplayStores**
</dt> <dd>

O número de armazenamentos de certificados na **matriz rghDisplayStores.**

</dd> <dt>

**rghDisplayStores**
</dt> <dd>

Um ponteiro para uma matriz de armazenamentos que contêm certificados disponíveis para seleção na caixa de diálogo.

</dd> <dt>

**cStores**
</dt> <dd>

O número de armazenamentos de certificados na **matriz rghStores.**

</dd> <dt>

**rghStores**
</dt> <dd>

Um ponteiro para uma matriz de armazenamentos de certificados a serem pesquisados ao criar uma cadeia de certificados e verificar a confiança dos certificados exibidos na caixa de diálogo.

</dd> <dt>

**cPropSheetPages**
</dt> <dd>

O número de páginas de propriedades na **matriz rgPropSheetPages.**

</dd> <dt>

**rgPropSheetPages**
</dt> <dd>

Um ponteiro para uma matriz de estruturas **PROPSHEETPAGE** que representam páginas de propriedades que são passadas para a caixa de diálogo de exibição de certificado quando um certificado é selecionado para exibição.

</dd> <dt>

**hSelectedCertStore**
</dt> <dd>

Um handle para um armazenamento de certificados criado pelo chamador. Os certificados selecionados pelo usuário são adicionados a esse armazenamento. Se o número de certificados nesse armazenamento for o mesmo antes e depois de chamar [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), o usuário fechou a caixa de diálogo sem selecionar nenhum certificado.

Esse membro não será usado se **o membro dwFlags** dessa estrutura não contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MULTISELECT.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                            |
| Nomes Unicode e ANSI<br/>   | **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) e **CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




