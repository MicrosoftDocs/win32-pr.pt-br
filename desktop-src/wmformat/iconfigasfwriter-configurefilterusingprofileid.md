---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileId
description: O método ConfigureFilterUsingProfileId configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema. (somente para perfis do formato de mídia Windows 4,0.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfileId
- Método ConfigureFilterUsingProfileId Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6321d259a213426df7e4490c3fc8a793e583a6fcdf58ec795a9f88e43645377f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028480"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Método IConfigAsfWriter:: ConfigureFilterUsingProfileId

O método **ConfigureFilterUsingProfileId** configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema. (somente para perfis do formato de mídia Windows 4,0.)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwProfileId* \[ no\]
</dt> <dd>

ID do perfil, conforme definido na versão 4,0 do SDK do formato de mídia Windows.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                         | Descrição                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ falha**</dt> </dl>              | O perfil não é válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl> | O grafo de filtro é interrompido.<br/> |



 

## <a name="remarks"></a>Comentários

este método agora é obsoleto porque ele pressupõe a versão 4,0 Windows perfis do SDK do formato de mídia. Para configurar o filtro para a versão 7,0 e perfis posteriores, use [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) ou [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

