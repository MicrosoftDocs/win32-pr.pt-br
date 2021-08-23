---
title: Mensagem de TB_SETIMAGELIST (commctrl. h)
description: Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em seu estado padrão.
ms.assetid: 432ffdfc-bb63-4405-90da-9392910fdbb6
keywords:
- controles de Windows de mensagem de TB_SETIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a7110084f2abe39cbae51815d1e59972cb016ea267275f0481d21e1f8b908a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167456"
---
# <a name="tb_setimagelist-message"></a>Mensagem de TB \_ SETimagelist

Define a lista de imagens que a barra de ferramentas usa para exibir botões que estão em seu estado padrão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

[Versão 5,80.](common-control-versions.md) O índice da lista. Se você usar apenas uma lista de imagens ou uma versão anterior dos controles comuns, defina *wParam* como zero. Consulte comentários para obter detalhes sobre como usar várias listas de imagens.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a lista de imagens a ser definida. Se esse parâmetro for **nulo**, nenhuma imagem será exibida nos botões.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para a lista de imagens usada anteriormente para exibir botões em seu estado padrão, ou **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.

## <a name="remarks"></a>Comentários

> [!Note]  
> Seu aplicativo é responsável por liberar a lista de imagens depois que a barra de ferramentas é destruída.

 

A mensagem de **TB \_ SetImageList** não pode ser combinada com [**TB \_ AddBitmap**](tb-addbitmap.md). Ele também não pode ser usado com barras de ferramentas criadas com [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), que chama **TB \_ AddBitmap** internamente. Quando você cria uma barra de ferramentas com **CreateToolbarEx** ou usa **TB \_ AddBitmap** para adicionar imagens, a barra de ferramentas gerencia a lista de imagens internamente. A tentativa de modificá-lo com **TB \_ SetImageList** tem consequências imprevisíveis.

Com a [versão 5,80](common-control-versions.md) ou posterior dos controles comuns, as imagens de botão não precisam vir da mesma lista de imagens. Para usar várias listas de imagens para suas imagens de botão da barra de ferramentas:

1.  Habilite várias listas de imagens enviando a barra de ferramentas controle uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) com *wParam* (o número de versão) definido como 5.
2.  Para cada lista de imagens que você deseja usar, envie a barra de ferramentas para o controle de uma mensagem de **TB \_ SetImageList** . Defina *wParam* como um valor *wParam* definido pelo aplicativo que será usado para identificar a lista. Defina *lParam* como o identificador HIMAGELIST da lista.
3.  Para cada botão, defina o membro **iBitmap** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) do botão como MAKELONG (*iIndex*, *iImageID*). O valor de *iImageID* é a ID da lista de imagens apropriada que foi definida na etapa dois. O valor de *iIndex* é o índice da imagem específica dentro dessa lista.
4.  Adicione os botões enviando a barra de ferramentas o controle uma mensagem de [**\_ rebotão de TB**](tb-addbuttons.md) .

O fragmento de código a seguir ilustra como adicionar cinco botões a uma barra de ferramentas, com imagens de três listas de imagens diferentes. O suporte para várias listas de imagens é habilitado com uma mensagem [**CCM \_ SetVersion**](ccm-setversion.md) . As listas de imagens são, então, definidas e atribuídas IDs de 0-2. Os botões recebem imagens das listas de imagens da seguinte maneira:

-   O botão 0 é da lista de imagens zero (ahim \[ 0 \] ) com o índice de 1.
-   O botão 1 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 1.
-   O botão 2 é da lista de imagens dois (ahim \[ 2 \] ) com um índice de 1.
-   O botão 3 é da lista de imagens zero (ahim \[ 0 \] ) com um índice de 2.
-   O botão 4 é da lista de imagens um (ahim \[ 1 \] ) com um índice de 3.

Por fim, os botões são adicionados ao controle barra de ferramentas com uma mensagem de [**\_ hiperbotãos de TB**](tb-addbuttons.md) .


```
//Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))
</dt> </dl>

 

