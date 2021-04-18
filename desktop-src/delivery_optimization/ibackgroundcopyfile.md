---
title: Interface IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contém informações sobre um arquivo que faz parte de um trabalho. Por exemplo, você pode usar métodos IBackgroundCopyFile para recuperar os nomes locais e remotos do arquivo e transferir as informações de progresso.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761524"
---
# <a name="ibackgroundcopyfile-interface"></a>Interface IBackgroundCopyFile

**IBackgroundCopyFile** contém informações sobre um arquivo que faz parte de um trabalho. Por exemplo, você pode usar métodos **IBackgroundCopyFile** para recuperar os nomes locais e remotos do arquivo e transferir as informações de progresso.

Para obter um ponteiro de interface **IBackgroundCopyFile** , chame o método [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) ou o método [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .

## <a name="members"></a>Membros

A interface **IBackgroundCopyFile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyFile** tem esses métodos.



| Método                                                            | Descrição                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**Getlocalname**](ibackgroundcopyfile-getlocalname-method.md)   | Recupera o nome local do arquivo.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Recupera o progresso da transferência de arquivo.<br/> |
| [**Getremotename**](ibackgroundcopyfile-getremotename-method.md) | Recupera o nome remoto do arquivo.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

