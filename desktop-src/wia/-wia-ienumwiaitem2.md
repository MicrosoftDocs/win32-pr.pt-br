---
description: Usado por aplicativos para enumerar objetos IWiaItem2 na pasta atual da árvore de itens.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interface IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752608"
---
# <a name="ienumwiaitem2-interface"></a>Interface IEnumWiaItem2

Usado por aplicativos para enumerar objetos [**IWiaItem2**](-wia-iwiaitem2.md) na pasta atual da árvore de itens.

## <a name="members"></a>Membros

A interface **IEnumWiaItem2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumWiaItem2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumWiaItem2** tem esses métodos.



| Método                                          | Descrição                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**8i**](-wia-ienumwiaitem2-clone.md)       | Cria uma instância adicional da interface **IEnumWiaItem2** e envia de volta um ponteiro para ela. <br/>                  |
| [**GetCount**](-wia-ienumwiaitem2-getcount.md) | Retorna o número de elementos armazenados por este enumerador. <br/>                                                          |
| [**Avançar**](-wia-ienumwiaitem2-next.md)         | Preenche uma matriz de ponteiros para interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .<br/>                                       |
| [**Redefinir**](-wia-ienumwiaitem2-reset.md)       | Redefine a referência de enumeração para o primeiro objeto [**IWiaItem2**](-wia-iwiaitem2.md) . <br/>                          |
| [**Ignorar**](-wia-ienumwiaitem2-skip.md)         | Ignora o número especificado de itens durante uma enumeração de objetos [**IWiaItem2**](-wia-iwiaitem2.md) disponíveis.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
