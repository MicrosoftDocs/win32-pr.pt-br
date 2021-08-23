---
title: Método NewConfig INapComponentConfig3 (NapCommon.h)
description: É implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- NAP do método NewConfig
- Método NewConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP , método NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff87f55218d8c84b1cb95a75e1801783e57b17288c36057323589ab44a47d3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891336"
---
# <a name="inapcomponentconfig3newconfig-method"></a>Método INapComponentConfig3::NewConfig

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O **método NewConfig** é implementado por SHVs (validadores de saúde do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica. Quando essa função é chamada, um SHV deve alocar novos dados de configuração e populá-los com uma cópia dos dados de configuração padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configID* 
</dt> <dd>

Um valor que representa a configuração. *ConfigID* é atribuído pelo serviço NPS (Servidor de Políticas de Rede) e é exclusivo dentro do SHV.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos códigos de erro a seguir com base no resultado dessa operação.



| Código de retorno                                                                                                 | Descrição                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | A operação teve êxito.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* é 0 (um valor reservado para a configuração padrão).<br/>                  |
| <dl> <dt>**NAP \_ E \_ SHV \_ CONFIG \_ EXISTE**</dt> </dl> | *ConfigID* já existe. A lista de IDs conhecidas pelo NPS é diferente da SHV.<br/> |



 

## <a name="remarks"></a>Comentários

Depois que a nova configuração for criada por **NewConfig,** os métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) deverão ser usados para alterar a configuração conforme necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





