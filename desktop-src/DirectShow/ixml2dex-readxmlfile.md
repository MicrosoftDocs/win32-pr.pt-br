---
description: O método ReadXMLfile carrega um arquivo de projeto XML.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'Método IXml2Dex:: ReadXMLfile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952435"
---
# <a name="ixml2dexreadxmlfile-method"></a>Método IXml2Dex:: ReadXMLfile

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ReadXMLFile` método carrega um arquivo de projeto XML. Esse método cria instâncias de todos os objetos expressos no arquivo XML e os insere na linha do tempo, bem como aplica os atributos fornecidos para a linha do tempo, como a taxa de quadros ou o efeito padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de um objeto de linha do tempo.

</dd> <dt>

*XMLName* 
</dt> <dd>

Cadeia de caracteres que especifica o nome do arquivo a ser carregado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor HRESULT. Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                                  | Descrição                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito<br/>             |
| <dl> <dt>**VFW \_ E \_ \_ formato de arquivo inválido \_**</dt> </dl> | Formato de arquivo inválido<br/> |



 

## <a name="remarks"></a>Comentários

Esse método não limpa os objetos existentes da linha do tempo antes de inserir os novos objetos definidos no arquivo XML. Se você precisar atualizar uma linha do tempo existente, chame [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) primeiro.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Internet Explorer 4,0 ou posterior<br/>                                               |
| Cabeçalho<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




