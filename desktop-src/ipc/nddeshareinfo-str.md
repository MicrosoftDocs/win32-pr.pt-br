---
description: Contém atributos de compartilhamento DDE mantidos pelo NetDDE Share Database Manager (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estrutura NDINFOAREINFO (Nddeapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 84d29bcf5e1e4d086ca60da619edf26640c583f238d4fa956b3edd696eceee1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481706"
---
# <a name="nddeshareinfo-structure"></a>Estrutura ND KAMAREINFO

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ NOT \_ IMPLEMENTED.\]

Contém atributos de compartilhamento DDE mantidos pelo NetDDE Share Database Manager (DSDM). O descritor de segurança associado a cada compartilhamento DDE não é passado por essa estrutura, mas é acessado por meio de funções específicas. A API do NetDDE DSDM aceita essa estrutura para funções definidas; para obter funções, o DSDM retorna a estrutura empacotada no buffer fornecido juntamente com os dados referenciados pelos membros **lpszShareName**, **lpszAppTopicList** e **lpszItemList**.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**lRevision**
</dt> <dd>

O nível de revisão da **estrutura NDINFOAREINFO.** Atualmente, o nível de revisão é 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

O nome do compartilhamento. Essa cadeia de caracteres não deve ter mais que os caracteres \_ MAX ND LTDARENAME.

</dd> <dt>

**lShareType**
</dt> <dd>

Um ou mais tipos de compartilhamento DDE. Esse membro pode ser uma combinação dos seguintes tipos de compartilhamento DDE com suporte.



| Tipo de compartilhamento                                                                                                                                                                                                                           | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**COMPARTILHAR \_ DIGITE \_ NOVO**</dt> <dt>0X02</dt> </dl>          | O compartilhamento contém um par aplicativo/tópico OLE.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**COMPARTILHAR \_ DIGITE \_ OLD**</dt> <dt>0x01</dt> </dl>          | O compartilhamento contém um par de aplicativos/tópicos DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**COMPARTILHAR \_ TYPE \_ STATIC**</dt> <dt>0x04</dt> </dl> | O compartilhamento contém um par de aplicativos/tópicos estáticos.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo para os pares DDE, OLE e aplicativo/tópico estático. O buffer deve estar no seguinte formato:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Se esse membro for **FALSE,** o compartilhamento DDE não permitirá que os usuários remotos se comuniquem por meio dele usando dde. No entanto, os usuários locais ainda podem se comunicar por meio do compartilhamento DDE. Os links do cliente local sempre serão implícitos se a DACL associada conceder acesso.

</dd> <dt>

**fService**
</dt> <dd>

Se esse membro for definido, o compartilhamento DDE não verificará se o usuário atual o definiu como confiável antes de permitir a comunicação DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Se esse membro for definido e o compartilhamento for confiável para iniciar aplicativos, o NetDDE tentará iniciar o aplicativo especificado por **lpszAppTopicList** se ele não puder iniciar inicialmente uma conversa DDE com o aplicativo.

</dd> <dt>

**Ncmdshow**
</dt> <dd>

Quando o NetDDE inicia um aplicativo para iniciar uma conversa DDE, esse valor é enviado ao aplicativo por meio do parâmetro *nCmdShow* da [**função WinMain.**](/windows/win32/api/winbase/nf-winbase-winmain) Ele define o modo preferencial para a janela do aplicativo a ser mostrada. Esse parâmetro só será significativo se **fStartAppFlag** estiver ativo. O usuário conectado no cujo contexto o aplicativo é iniciado também pode substituir essa opção ao promover o compartilhamento para o status confiável. O padrão para esse membro é SW \_ SHOWMAXIMIZED.

</dd> <dt>

**qModifyId**
</dt> <dd>

Um número de série de 8 byte que indica o número de série de modificação do compartilhamento DDE. Sempre que o compartilhamento DDE é modificado por [**uma chamada NDdeShareSetInfo**](nddesharesetinfo.md) ou [**NDdeSetShareSecurity,**](nddesetsharesecurity.md) esses valores são alterados.

</dd> <dt>

**cNumItems**
</dt> <dd>

O número de itens **listados em lpszItemList.** Se **cNumItems** for zero, **lpszItemList** será vazio e as informações de compartilhamento e o descritor de segurança associado se aplicarão a todos os itens atendidos pelo aplicativo associado.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo que especificam os itens que o aplicativo cliente em uma transação DDE pode solicitar ou iniciar loops de consultoria. Se nenhum item estiver listado, o compartilhamento DDE permitirá que qualquer item seja usado. O número de itens na lista deve corresponder à **contagem de cNumItems.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Estruturas DDE de rede](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

