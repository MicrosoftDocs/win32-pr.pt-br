---
description: Estrutura DEVICEDIALOGDATA – define os dados necessários para chamar uma caixa de diálogo do dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Estrutura DEVICEDIALOGDATA (Wiadefd.h)
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
ms.openlocfilehash: e20b8689e71031024c46451d3079450061e8112acf1052c12129b89ed9e0a23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451196"
---
# <a name="devicedialogdata-structure"></a>Estrutura DEVICEDIALOGDATA

Define os dados necessários para chamar uma caixa de diálogo do dispositivo.

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

**Hwndparent**
</dt> <dd>

Digite: **HWND**

</dd> <dd>

Especifica o alça para a janela pai da caixa de diálogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***

</dd> <dd>

Aponta para uma interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa o item raiz válido na árvore de itens do aplicativo.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica um conjunto de sinalizadores que controlam a operação da caixa de diálogo. Pode ser definido como qualquer um dos seguintes valores:



| Sinalizador                                 | Significado                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento padrão.                                                                                                                                                                           |
| IMAGEM ÚNICA DA CAIXA DE \_ \_ DIÁLOGO \_ DISPOSITIVO \_ WIA   | Restrinja a seleção de imagem a uma única imagem na caixa de diálogo de aquisição de imagem do dispositivo.                                                                                                      |
| CAIXA DE DIÁLOGO \_ \_ DISPOSITIVO WIA USAR INTERFACE \_ DO USUÁRIO \_ \_ COMUM | Use a interface do usuário do sistema, se disponível, em vez da interface do usuário fornecida pelo fornecedor. Se a interface do usuário do sistema não estiver disponível, a interface do usuário do fornecedor será usada. Se nenhuma das interfaces do usuário estiver disponível, a função retornará E \_ NOTIMPL. |



 

</dd> <dt>

**lIntent**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Especifica que tipo de dados a imagem deve representar. Para ver uma lista de valores de intenção de imagem, consulte [**Constantes de intenção de imagem**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Recebe o número de itens na matriz indicado pelo **parâmetro ppWiaItem.**

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Recebe o endereço de uma matriz de ponteiros para interfaces [**IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




