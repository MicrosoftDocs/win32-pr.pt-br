---
description: Contém atributos de compartilhamento DDE mantidos pelo Gerenciador de banco de dados de compartilhamento NetDDE (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Estrutura NDDESHAREINFO (Nddeapi. h)
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
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812187"
---
# <a name="nddeshareinfo-structure"></a>Estrutura NDDESHAREINFO

\[Não há mais suporte para DDE de rede. Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]

Contém atributos de compartilhamento DDE mantidos pelo Gerenciador de banco de dados de compartilhamento NetDDE (DSDM). O descritor de segurança associado a cada compartilhamento DDE não é passado por essa estrutura, mas é acessado por meio de funções específicas. A API do NetDDE DSDM aceita essa estrutura para funções Set; para funções Get, o DSDM retorna a estrutura empacotada no buffer fornecido junto com os dados referenciados pelos membros **lpszShareName**, **lpszAppTopicList** e **lpszItemList**.

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

O nível de revisão da estrutura **NDDESHAREINFO** . Atualmente, o nível de revisão é 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

O nome do compartilhamento. Essa cadeia de caracteres não deve ter mais do que o máximo de \_ NDDESHARENAME caracteres.

</dd> <dt>

**lShareType**
</dt> <dd>

Um ou mais tipos de compartilhamento DDE. Esse membro pode ser uma combinação dos seguintes tipos de compartilhamento de DDE com suporte.



| Tipo de compartilhamento                                                                                                                                                                                                                           | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**Compartilhar \_ Digite \_ novo**</dt> <dt>0x02</dt> </dl>          | O compartilhamento contém um par de aplicativo/tópico OLE.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**Compartilhar \_ Digite \_ antigo**</dt> <dt>0x01</dt> </dl>          | O compartilhamento contém um par de aplicativo/tópico DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**Compartilhar \_ Digite \_**</dt> <dt>0x04</dt> estático </dl> | O compartilhamento contém um par de aplicativo/tópico estático.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo para os pares de aplicativo/tópico estáticos, OLE e DDE. O buffer deve estar no seguinte formato:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Se esse membro for **falso**, o compartilhamento DDE não permitirá que os usuários remotos se comuniquem através dele usando o DDE. No entanto, os usuários locais ainda podem se comunicar por meio do compartilhamento DDE. Os links de cliente local serão sempre inferidos se a DACL associada conceder acesso.

</dd> <dt>

**fService**
</dt> <dd>

Se esse membro estiver definido, o compartilhamento DDE não verificará se o usuário atual o definiu como confiável antes de permitir a comunicação DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Se esse membro estiver definido e o compartilhamento for confiável para iniciar aplicativos, o NetDDE tentará iniciar o aplicativo especificado por **lpszAppTopicList** se ele não puder iniciar inicialmente uma conversa DDE com o aplicativo.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Quando o NetDDE inicia um aplicativo para iniciar uma conversa DDE, esse valor é enviado para o aplicativo por meio do parâmetro *nCmdShow* da função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) . Ele define o modo preferencial para a janela do aplicativo a ser mostrada no. Esse parâmetro será significativo somente se **fStartAppFlag** estiver ativo. O usuário conectado em cujo contexto o aplicativo é iniciado também pode substituir essa opção ao promover o compartilhamento para o status confiável. O padrão para esse membro é SW \_ PERmaximed.

</dd> <dt>

**qModifyId**
</dt> <dd>

Um número de série de 8 bytes que indica o número de série de modificação do compartilhamento DDE. Toda vez que o compartilhamento DDE é modificado por uma chamada [**NDdeShareSetInfo**](nddesharesetinfo.md) ou [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , esses valores são alterados.

</dd> <dt>

**cNumItems**
</dt> <dd>

O número de itens listados em **lpszItemList**. Se **cNumItems** for zero, **lpszItemList** estará vazio e as informações de compartilhamento e o descritor de segurança associado serão aplicados a todos os itens atendidos pelo aplicativo associado.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Um ponteiro para um buffer que contém cadeias de caracteres terminadas em nulo que especificam os itens em que o aplicativo cliente em uma transação DDE pode solicitar ou iniciar loops de aviso. Se nenhum item estiver listado, o compartilhamento de DDE permitirá que todos os itens sejam usados. O número de itens na lista deve corresponder à contagem de **cNumItems** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral de troca dinâmica de dados de rede](network-dynamic-data-exchange.md)
</dt> <dt>

[Estruturas DDE de rede](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

