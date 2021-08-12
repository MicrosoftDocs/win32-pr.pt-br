---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon.h)
description: É implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- NAP do método DeleteAllConfig
- Método NAP DeleteAllConfig, interface INapComponentConfig3
- INapComponentConfig3 interface NAP , método DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b2a81a33dfb659c3398c8c853132244d088b7fa65bd4bb0317869e13b85abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621735"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>Método INapComponentConfig3::D eleteAllConfig

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método DeleteAllConfig** é implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação. Todos os dados de configuração, exceto a configuração padrão, devem ser excluídos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos códigos de erro a seguir com base no resultado dessa operação.



| Código de retorno                                                                           | Descrição                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | A operação teve êxito.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





