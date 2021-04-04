---
title: Método INapComponentConfig3 NewConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Método NewConfig NAP
- Método NewConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método NewConfig
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
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085372"
---
# <a name="inapcomponentconfig3newconfig-method"></a>Método INapComponentConfig3:: NewConfig

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **newconfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de criar dados de configuração para uma ID de configuração específica. Quando essa função é chamada, um SHV deve alocar novos dados de configuração e preenchê-lo com uma cópia dos dados de configuração padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configid* 
</dt> <dd>

Um valor que representa a configuração. *Configid* é atribuído pelo serviço NPS (servidor de políticas de rede) e é exclusivo dentro do SHV.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                                 | Descrição                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | A operação teve êxito.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *Configid* é 0 (um valor reservado para a configuração padrão).<br/>                  |
| <dl> <dt>**a \_ configuração de NAP E \_ SHV \_ \_ existia**</dt> </dl> | *Configid* já existe. A lista de IDs conhecida pelo NPS é diferente do SHV.<br/> |



 

## <a name="remarks"></a>Comentários

Depois que a nova configuração é criada por **newconfig**, os métodos [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)e [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) devem ser usados para alterar a configuração conforme necessário.

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

 

 





