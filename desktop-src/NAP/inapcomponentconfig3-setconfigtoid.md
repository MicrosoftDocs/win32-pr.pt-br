---
title: Método INapComponentConfig3 SetConfigToID (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Método SetConfigToID NAP
- Método SetConfigToID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010fdc6cbb236a113e4f1804d3a4780c0e6a72f89b1f03bf90f1d99a92dc2bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781076"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>Método INapComponentConfig3:: SetConfigToID

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **SetConfigToID** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de definir os dados de configuração para uma ID de configuração específica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*configid* \[ no\]
</dt> <dd>

Um valor que representa a configuração. *Configid* é atribuído pelo serviço NPS (servidor de políticas de rede) e é exclusivo dentro do SHV. Se *configid* for 0, a configuração padrão do SHV será definida.

</dd> <dt>

*contagem* \[ de no\]
</dt> <dd>

O tamanho, em bytes, dos dados de configuração nos *dados*.

</dd> <dt>

*dados* \[ do no\]
</dt> <dd>

Na entrada, uma matriz de bytes que contém os dados de configuração definidos como *configid*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                                    | Descrição                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | A operação teve êxito.<br/> |
| <dl> <dt>**configuração de NAP \_ E \_ SHV \_ \_ não \_ encontrada**</dt> </dl> | Não foi possível encontrar *configid* .<br/>  |



 

## <a name="remarks"></a>Comentários

O método [**newconfig**](inapcomponentconfig3-newconfig.md) deve ser usado para alocar dados de configuração para *configid* antes que este método possa ser chamado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





