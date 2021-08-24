---
title: Interface IBackgroundCopyFile2 (Deliveryoptimization.h)
description: Use a interface IBackgroundCopyFile2 para especificar um novo nome remoto para o arquivo e recuperar a lista de intervalos a baixar.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f185fef1ddaa9ceb4298f3e8916bb3d207b311b300f0071d601aadf47b0777a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853856"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interface IBackgroundCopyFile2

Use a interface **IBackgroundCopyFile2** para especificar um novo nome remoto para o arquivo e recuperar a lista de intervalos a baixar.

A interface **IBackgroundCopyFile2** herda da interface [**IBackgroundCopyFile.**](ibackgroundcopyfile.md)

Para obter um ponteiro de interface **IBackgroundCopyFile2,** chame o método **IBackgroundCopyFile::QueryInterface** usando __uuidof(IBackgroundCopyFile2) para o identificador de interface. Use o ponteiro da interface **IBackgroundCopyFile2** para chamar os métodos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2.**

## <a name="members"></a>Membros

A interface **IBackgroundCopyFile2** herda de [**IBackgroundCopyFile.**](ibackgroundcopyfile.md) **IBackgroundCopyFile2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyFile2** tem esses métodos.



| Método                                                             | Descrição                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Recupera a matriz de intervalos que você deseja baixar da URL.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Altera o nome remoto para uma nova URL.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 é definido como 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





