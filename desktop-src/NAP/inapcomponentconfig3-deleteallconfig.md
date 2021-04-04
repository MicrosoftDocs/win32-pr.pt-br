---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Método DeleteAllConfig NAP
- Método DeleteAllConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método DeleteAllConfig
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
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824290"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3: método eleteAllConfig de:D

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **DeleteAllConfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação. Todos os dados de configuração, exceto a configuração padrão, devem ser excluídos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                           | Descrição                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | A operação teve êxito.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





