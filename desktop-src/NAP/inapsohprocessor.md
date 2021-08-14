---
title: Interface INapSoHProcessor (NapProtocol. h)
description: São usados por SHAs para processar o conteúdo de SoHResponses e por SHVs para processar o conteúdo de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- INapSoHProcessor da interface NAP
- INapSoHProcessor interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca4a87e15d3810605038231eaec066e9f26ed079aca0d0715c72e7c69ed8d600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799478"
---
# <a name="inapsohprocessor-interface"></a>Interface INapSoHProcessor

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O **INapSoHProcessor** fornece métodos que são usados por SHAs para processar o conteúdo de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) e por SHVs para processar o conteúdo de **SoHRequests**.

## <a name="members"></a>Membros

A interface **INapSoHProcessor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapSoHProcessor** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **INapSoHProcessor** tem esses métodos.



| Método                                                                                           | Descrição                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md)         | Localiza o índice de localização do próximo atributo de pacote SoH.<br/>                 |
| [**INapSoHProcessor:: GetAttribute**](inapsohprocessor-getattribute-method.md)                   | Recupera o tipo de atributo e o valor.<br/>                                    |
| [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md) | Recupera o número de atributos contidos na SoH.<br/>                   |
| [**INapSoHProcessor:: Initialize**](inapsohprocessor-initialize-method.md)                       | Inicializa o pacote de protocolo SoH e o sistema NAP para processamento de conteúdo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Referência de NAP](nap-reference.md)
</dt> </dl>

 

