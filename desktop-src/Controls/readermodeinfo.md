---
title: Estrutura READERMODEINFO
description: Contém as informações necessárias para inicializar a função doreadermode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Controles do Windows da estrutura READERMODEINFO
- Controles do Windows de ponteiro de estrutura PREADERMODEINFO
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455525"
---
# <a name="readermodeinfo-structure"></a>Estrutura READERMODEINFO

\[O **READERMODEINFO** é compatível com o Windows XP com Service Pack 2 (SP2). Ele pode não ter suporte em versões subsequentes.\]

Contém as informações necessárias para inicializar a função [**Doreadermode**](doreadermode.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obrigatórios. O tamanho da estrutura, em bytes. Defina esse parâmetro como **sizeof (readermode) antes de** chamar [**doreadermode**](doreadermode.md).

</dd> <dt>

**HWND**
</dt> <dd>

Tipo: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Obrigatórios. O identificador da janela a ser usada para o modo de leitura.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Sinalizadores que personalizam a funcionalidade da janela do modo de leitura. Esse parâmetro pode ser 0; caso contrário, um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                  | Significado                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt> </dl>             | Define o cursor no centro da área especificada na **prc**. Se esse sinalizador não for especificado, a posição do cursor permanecerá inalterada.<br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt> </dl>       | Permite apenas a rolagem vertical.<br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt> </dl> | Permite apenas a rolagem horizontal.<br/>                                                                                                     |



 

</dd> <dt>

**popular**
</dt> <dd>

Tipo: **lpRect**

</dd> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica a área de rolagem na janela modo de leitor. Se esse membro for **nulo**, a janela inteira será usada como a área de rolagem.

</dd> <dt>

**pfnScroll**
</dt> <dd>

Tipo: **PFNREADERSCROLL**

</dd> <dd>

Um ponteiro para uma função de retorno de chamada [*ReaderScroll*](readerscroll.md) definida pelo aplicativo usado para notificar o aplicativo que a janela precisa ser rolada em uma direção específica.

</dd> <dt>

**fFlags**
</dt> <dd>

Tipo: **PFNREADERTRANSLATEDISPATCH**

</dd> <dd>

Um ponteiro para uma função de retorno de chamada [*TranslateDispatch*](translatedispatch.md) definida pelo aplicativo usada para obter a primeira notificação de todas as mensagens enviadas para a janela do modo de leitura.

</dd> <dt>

**lParam**
</dt> <dd>

Tipo: **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Informações adicionais conforme necessário pelo aplicativo, lidas pelo chamador na função de retorno de chamada [*ReaderScroll*](readerscroll.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura não é declarada em nenhum cabeçalho público. Para usá-lo, você deve incluir a declaração mostrada acima em seu próprio cabeçalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>          |



 

