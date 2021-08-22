---
description: Estrutura DEVICEDIALOGDATA2 – define os dados necessários para chamar uma caixa de diálogo de dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Estrutura DEVICEDIALOGDATA2 (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 800f7ceb102cafcad8ddda5204990706b908a4a0137a16143af76a90345b472e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451186"
---
# <a name="devicedialogdata2-structure"></a>Estrutura DEVICEDIALOGDATA2

Define os dados necessários para chamar uma caixa de diálogo de dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Especifica o tamanho dessa estrutura em bytes.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Aponta para uma interface [**IWiaItem2**](-wia-iwiaitem2.md) que representa o item raiz válido na árvore de itens de aplicativo.

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

**hwndParent**
</dt> <dd>

Digite: **HWND**

</dd> <dd>

Especifica o identificador para a janela pai da caixa de diálogo.

</dd> <dt>

**bstrFolderName**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Especifica o nome da pasta onde os arquivos são transferidos.

</dd> <dt>

**bstrFilename**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Especifica o modelo de nome de arquivo a ser usado para arquivos transferidos de itens WIA para a pasta de destino designada por **bstrFolderName**. Um número arbitrário de nomes de arquivo exclusivos pode ser criado acrescentando-se caracteres adicionais ao modelo de nome de arquivo.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Tipo: **longo**

</dd> <dd>

Recebe o número de cadeias de caracteres gravadas na matriz **pbstrFilePaths** .

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Tipo: **BSTR \***

</dd> <dd>

Ponteiro para uma matriz de ponteiros BSTR. Cada elemento de matriz aponta para um BSTR que contém o nome de destino de um arquivo que foi transferido com êxito para a pasta identificada por bstrFolderName. O método deve alocar o armazenamento para esse membro.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item WIA que transfere dados para o arquivo ou arquivos nomeados na matriz **pbstrFilePaths** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




