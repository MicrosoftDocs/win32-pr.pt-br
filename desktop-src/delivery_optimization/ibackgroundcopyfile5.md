---
title: Interface IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Use essa interface para obter ou definir propriedades genéricas de transferências de arquivos de otimização de entrega.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085476"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interface IBackgroundCopyFile5

Use essa interface para obter ou definir propriedades genéricas de transferências de arquivos de otimização de entrega.

Para obter um ponteiro de interface **IBackgroundCopyFile5** , chame o método **IBackgroundCopyFile:: QueryInterface** usando __uuidof (IBackgroundCopyFile5) para o identificador de interface.

## <a name="members"></a>Membros

A interface **IBackgroundCopyFile5** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile5** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyFile5** tem esses métodos.



| Método                                                  | Descrição                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Obtém o valor de uma propriedade BackgroundCopyFile genérica.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Define o valor de uma propriedade BackgroundCopyFile genérica.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 é definido como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

