---
description: A interface IPropertySetter define propriedades em um efeito ou transição DirectShow DeS (Serviços de Edição). Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID PropertySetter) e associe-a a um efeito ou transição chamando o método \_ IAMTimelineObj::SetPropertySetter. Para obter mais informações, consulte Trabalhando com efeitos e transições. Normalmente, um aplicativo precisa chamar apenas o método IPropertySetter::ClearProps para limpar as propriedades existentes e o método IPropertySetter::AddProp para adicionar novas propriedades. Os outros métodos nessa interface são chamados por outros componentes do DES.
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interface IPropertySetter (Qedit.h)
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
ms.openlocfilehash: c6dc32c25c85893eeb2e9872bcf67be974489ec82fdd4d09c19a2341f6867ade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831026"
---
# <a name="ipropertysetter-interface"></a>Interface IPropertySetter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IPropertySetter` interface define propriedades em um efeito ou transição DirectShow [DES (Serviços](directshow-editing-services.md) de Edição).

Para usar essa interface, crie uma instância de um objeto setter de propriedade (CLSID PropertySetter) e associe-a a um efeito ou transição chamando o método \_ [**IAMTimelineObj::SetPropertySetter.**](iamtimelineobj-setpropertysetter.md) Para obter mais informações, [consulte Trabalhando com efeitos e transições.](working-with-effects-and-transitions.md)

Normalmente, um aplicativo precisa chamar apenas o método [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) para limpar as propriedades existentes e o método [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) para adicionar novas propriedades. Os outros métodos nessa interface são chamados por outros componentes do DES.

## <a name="members"></a>Membros

A interface **IPropertySetter** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPropertySetter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IPropertySetter** tem esses métodos.



| Método                                               | Descrição                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Adiciona uma propriedade ao setter de propriedade, com uma matriz de pares time-value definindo o valor da propriedade em um intervalo de tempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Limpa todos os dados de propriedade do setter de propriedade.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera os recursos alocados pelo [**método IPropertySetter::GetProps.**](ipropertysetter-getprops.md)<br/>                             |
| [**Getprops**](ipropertysetter-getprops.md)         | Recupera as propriedades definidas nesse objeto, com seus valores correspondentes.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carrega dados de propriedade de um formato de persistência.<br/>                                                                                     |
| [**Loadxml**](ipropertysetter-loadxml.md)           | Carrega dados de propriedade expressos em linguagem XML (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Converte dados de propriedade em uma cadeia de caracteres XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Salva os dados da propriedade em um formato de persistência.<br/>                                                                                   |
| [**Setprops**](ipropertysetter-setprops.md)         | Define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.<br/>                                          |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
