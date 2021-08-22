---
title: Método setconfig INapComponentConfig (NapCommon. h)
description: Define a configuração do componente do validador da integridade do sistema (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Método setconfig NAP
- Método setconfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método setconfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b3ecf455c591985a5e8778e49495351bd1b4aba83e9d29fe2b25d7d406a507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940194"
---
# <a name="inapcomponentconfigsetconfig-method"></a>Método INapComponentConfig:: setconfig

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **setconfig** define a configuração do componente do validador da integridade do sistema (SHV).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bCount* \[ no\]
</dt> <dd>

O tamanho, em bytes, do blob de configuração de *dados* .

</dd> <dt>

*dados* \[ do no\]
</dt> <dd>

Um ponteiro para os dados de configuração do componente SHV.

> [!Note]  
> Os dados de configuração exportados de um computador x86 usando o método [**GetConfig**](inapcomponentconfig-getconfig.md) podem ser importados para um computador x64 usando o método **setconfig** e vice-versa. Portanto, os dados de configuração devem estar em um formato independente de arquitetura, como XML. Usar XML em vez de um fluxo de bytes torna mais fácil usar dados de configuração em diferentes arquiteturas. Os elementos XML usados nos dados de configuração são determinados pelo implementador.

 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

As informações de controle de versão do componente devem ser incluídas no blob de configuração de *dados* . As informações de controle de versão podem ser usadas ao migrar de uma versão de SHV para outra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapConponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





