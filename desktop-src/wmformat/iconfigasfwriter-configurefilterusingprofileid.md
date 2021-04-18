---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileId
description: O método ConfigureFilterUsingProfileId configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema. (Somente para perfis do Windows Media Format 4,0.).
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
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105793827"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a>Método IConfigAsfWriter:: ConfigureFilterUsingProfileId

O método **ConfigureFilterUsingProfileId** configura o filtro para gravar um arquivo ASF com um índice de identificador de perfil (ID) da lista de perfis do sistema. (Somente para perfis do Windows Media Format 4,0.)

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

ID do perfil, conforme definido na versão 4,0 do SDK do Windows Media Format.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                         | Descrição                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ falha**</dt> </dl>              | O perfil não é válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl> | O grafo de filtro é interrompido.<br/> |



 

## <a name="remarks"></a>Comentários

Este método agora é obsoleto porque ele pressupõe os perfis do SDK do Windows Media Format versão 4,0. Para configurar o filtro para a versão 7,0 e perfis posteriores, use [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) ou [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

