---
title: Interface INapSoHConstructor (NapProtocol. h)
description: São usados por SHAs para construir SoHRequests e por SHVs para construir SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- INapSoHConstructor da interface NAP
- INapSoHConstructor interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918050"
---
# <a name="inapsohconstructor-interface"></a>Interface INapSoHConstructor

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapSoHConstructor** fornece métodos que são usados por SHAs para construir [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) e por SHVs para construir **SoHResponses**.

## <a name="members"></a>Membros

A interface **INapSoHConstructor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHConstructor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSoHConstructor** tem esses métodos.



| Método                                                                                   | Descrição                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [**INapSoHConstructor:: AppendAttribute**](inapsohconstructor-appendattribute-method.md) | Adiciona um TLV ao final do buffer SoH.<br/> |
| [**INapSoHConstructor::GetSoH**](inapsohconstructor-getsoh-method.md)                   | Recupera o pacote SoH construído.<br/>    |
| [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md)           | Inicializa o pacote SoH.<br/>              |
| [**INapSoHConstructor:: Validate**](inapsohconstructor-validate-method.md)               | Verifica a validade do pacote SoH.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

