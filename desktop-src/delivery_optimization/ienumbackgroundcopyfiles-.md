---
title: Interface IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Use a interface IEnumBackgroundCopyFiles para enumerar os arquivos que um trabalho contém. Para obter um ponteiro de interface IEnumBackgroundCopyFiles, chame o método método ibackgroundcopyjob EnumFiles.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, descrita
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105772522"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Interface IEnumBackgroundCopyFiles

Use a interface **IEnumBackgroundCopyFiles** para enumerar os arquivos que um trabalho contém. Para obter um ponteiro de interface **IEnumBackgroundCopyFiles** , chame o método [**método ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .

## <a name="members"></a>Membros

A interface **IEnumBackgroundCopyFiles** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumBackgroundCopyFiles** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IEnumBackgroundCopyFiles** tem esses métodos.



| Método                                                | Descrição                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Recupera o número de itens na enumeração.<br/>                  |
| [**Avançar**](ienumbackgroundcopyfiles-next.md)         | Recupera um número especificado de itens na sequência de enumeração.<br/> |
| [**Redefinir**](ienumbackgroundcopyfiles-reset.md)       | Redefine a sequência de enumeração para o início.<br/>                  |
| [**Ignorar**](ienumbackgroundcopyfiles-skip.md)         | Ignora um número especificado de itens na sequência de enumeração.<br/>     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob:: EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

