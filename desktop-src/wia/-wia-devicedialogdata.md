---
description: Define os dados necessários para chamar uma caixa de diálogo de dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estrutura DEVICEDIALOGDATA (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505895"
---
# <a name="devicedialogdata-structure"></a>Estrutura DEVICEDIALOGDATA

Define os dados necessários para chamar uma caixa de diálogo de dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica o tamanho dessa estrutura em bytes.

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **HWND**

</dd> <dd>

Especifica o identificador para a janela pai da caixa de diálogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _

</dd> <dd>

Aponta para uma interface [_ *IWiaItem* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa o item raiz válido na árvore de itens de aplicativo.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo. Pode ser definido como qualquer um dos seguintes valores:



| Sinalizador                                 | Significado                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento padrão.                                                                                                                                                                           |
| \_ \_ imagem única da caixa de diálogo do dispositivo WIA \_ \_   | Restringir a seleção de imagem a uma única imagem na caixa de diálogo aquisição de imagem de dispositivo.                                                                                                      |
| \_caixa de \_ diálogo do dispositivo WIA \_ usar \_ \_ interface do usuário comum | Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor. Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada. Se nenhuma interface do usuário estiver disponível, a função retornará E \_ NOTIMPL. |



 

</dd> <dt>

**lIntent**
</dt> <dd>

Tipo: **longo**

</dd> <dd>

Especifica o tipo de dados que a imagem deve representar. Para obter uma lista de valores de intenção de imagem, consulte [**constantes de objetivo de imagem**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **longo**

</dd> <dd>

Recebe o número de itens na matriz indicado pelo parâmetro **ppWiaItem** .

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Recebe o endereço de uma matriz de ponteiros para interfaces [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




