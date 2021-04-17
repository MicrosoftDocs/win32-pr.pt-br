---
description: Interrompe o coletor. Se o coletor estiver sendo executado como um serviço, a interrupção do serviço será a melhor abordagem.
ms.assetid: fab3e060-156f-46f5-98a2-d47a23d64552
ms.tgt_platform: multiple
title: Método Shutdown da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Shutdown
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d401ac528498d7b8ab5ccacbf6a0b5bf781555f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753849"
---
# <a name="shutdown-method-of-the-control-class"></a>Método Shutdown da classe Control

Interrompe o coletor. Se o coletor estiver sendo executado como um serviço, a interrupção do serviço será a melhor abordagem.

## <a name="syntax"></a>Sintaxe


```mof
void Shutdown();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controlo**](control.md)
</dt> </dl>

 

 




