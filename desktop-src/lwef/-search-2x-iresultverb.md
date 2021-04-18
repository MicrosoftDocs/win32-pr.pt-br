---
title: Interface IResultVerb (WdsSharedIDL. h)
description: Expõe as propriedades de verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Recursos do ambiente Windows herdado da interface IResultVerb
- Recursos do ambiente Windows herdado da interface IResultVerb, descritos
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781601"
---
# <a name="iresultverb-interface"></a>Interface IResultVerb

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Expõe as propriedades de verbo.

## <a name="members"></a>Membros

A interface **IResultVerb** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultVerb** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IResultVerb** tem essas propriedades.



| Propriedade                                                             | Tipo de acesso           | Descrição                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | Somente leitura<br/>  | Essa propriedade retorna um ponteiro para o nome de exibição localizado para o verbo. <br/>                           |
| [**DoIt**](-search-2x-iresultverb-doit.md)<br/>               | Somente gravação<br/> | Executa o verbo. <br/>                                                                                    |
| [**habilitado**](-search-2x-iresultverb-enabled.md)<br/>         | Somente leitura<br/>  | Essa propriedade retornará TRUE se o verbo estiver habilitado. <br/>                                                    |
| [**Texto**](-search-2x-iresultverb-helptext.md)<br/>       | Somente leitura<br/>  | Essa propriedade retorna um ponteiro para a cadeia de caracteres de ajuda localizada para o verbo. <br/>                            |
| [**ícone**](-search-2x-iresultverb-icon.md)<br/>               | Somente leitura<br/>  | Essa propriedade retorna um ponteiro para o identificador do ícone opcional associado ao verbo. <br/>              |
| [**Nome**](-search-2x-iresultverb-name.md)<br/>               | Somente leitura<br/>  | Essa propriedade retorna um ponteiro para o nome cononical do verbo, como Print, Open e assim por diante. <br/> |



 

## <a name="remarks"></a>Comentários

Esses métodos expõem propriedades e ações aplicáveis a verbos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]<br/>                             |
| Redistribuível<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| parâmetro<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

