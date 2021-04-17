---
title: Método IConfigAsfWriter ConfigureFilterUsingProfile
description: O método ConfigureFilterUsingProfile é a maneira recomendada para definir um perfil. Ele configura o filtro para gravar um arquivo ASF com base no perfil definido pelo aplicativo especificado.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfile
- Método ConfigureFilterUsingProfile Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761092"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>Método IConfigAsfWriter:: ConfigureFilterUsingProfile

O método **ConfigureFilterUsingProfile** é a maneira recomendada para definir um perfil. Ele configura o filtro para gravar um arquivo ASF com base no perfil definido pelo aplicativo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProfile* \[ no\]
</dt> <dd>

Ponteiro para a interface [**IWMProfile**](iwmprofile.md) no perfil definido pelo aplicativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                         | Descrição                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>           | O ponteiro de interface **IWMProfile** não é válido.<br/> |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl> | O grafo foi interrompido.<br/>                              |



 

## <a name="remarks"></a>Comentários

Se for bem-sucedido, esse método fará com que um evento **\_ \_ alterado de grafo do EC** seja enviado para o aplicativo. Use este método para configurar o gravador com um perfil personalizado do Windows Media 9 Series que você criou (ou carregou a partir de um arquivo. prx existente) usando os métodos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

