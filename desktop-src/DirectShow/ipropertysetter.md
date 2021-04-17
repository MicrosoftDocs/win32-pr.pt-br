---
description: 'A interface IPropertySetter define propriedades em um efeito ou transição nos serviços de edição do DirectShow (DES). Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID \_ PropertySetter) e associe-o a um efeito ou transição chamando o método IAMTimelineObj:: SetPropertySetter. Para obter mais informações, consulte trabalhando com efeitos e transições. geralmente um aplicativo precisa chamar apenas o método IPropertySetter:: ClearProps para limpar as propriedades existentes e o método IPropertySetter:: addprop para adicionar novas propriedades. Os outros métodos nessa interface são chamados por outros componentes DES.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interface IPropertySetter (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759534"
---
# <a name="ipropertysetter-interface"></a>Interface IPropertySetter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IPropertySetter` interface define as propriedades em um efeito ou uma transição nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).

Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID \_ PropertySetter) e associe-o a um efeito ou transição chamando o método [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) . Para obter mais informações, consulte [trabalhando com efeitos e transições](working-with-effects-and-transitions.md).

Normalmente, um aplicativo precisa chamar apenas o método [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) para limpar as propriedades existentes e o método [**IPropertySetter:: addprop**](ipropertysetter-addprop.md) para adicionar novas propriedades. Os outros métodos nessa interface são chamados por outros componentes DES.

## <a name="members"></a>Membros

A interface **IPropertySetter** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPropertySetter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPropertySetter** tem esses métodos.



| Método                                               | Descrição                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Addprop**](ipropertysetter-addprop.md)           | Adiciona uma propriedade ao setter de propriedade, com uma matriz de pares time-Value que definem o valor da propriedade em um intervalo de tempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Limpa todos os dados de Propriedade do setter de propriedade.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera recursos alocados pelo método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Recupera as propriedades definidas neste objeto com seus valores correspondentes.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carrega dados de propriedade de um formato de persistência.<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | Carrega dados de propriedade expressos em linguagem XML (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Converte dados de propriedade em uma cadeia de caracteres XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Salva os dados de propriedade em um formato de persistência.<br/>                                                                                   |
| [**Propriedades**](ipropertysetter-setprops.md)         | Define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.<br/>                                          |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
