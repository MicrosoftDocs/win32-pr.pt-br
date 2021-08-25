---
description: Fornece um modelo para criar fábricas de classes.
ms.assetid: 3dbe6402-15f8-4490-9fe2-bebaa4e79170
title: Classe CFactoryTemplate (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f9fbc76fe65e1f1136fb44d22db36500c4d8870f97befa8e36fa08a108ada71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697616"
---
# <a name="cfactorytemplate-class"></a>Classe CFactoryTemplate

Fornece um modelo para criar fábricas de classes.

no DirectShow, as fábricas de classe são especializadas usando a classe **CFactoryTemplate** , também chamada de *modelo de fábrica*. Cada fábrica de classe mantém um ponteiro para um modelo de fábrica. O modelo de fábrica contém informações sobre um objeto COM, incluindo o identificador de classe do objeto (CLSID) e um ponteiro para uma função que cria o objeto.

Em sua DLL, declare uma matriz global de modelos de fábrica chamada *g \_ templates*. Inclua um modelo de fábrica para cada objeto na DLL. Quando a função [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) cria uma nova fábrica de classes, ela pesquisa a matriz em busca de um modelo com um CLSID correspondente. Supondo que ele encontre um, ele cria uma fábrica de classes que mantém um ponteiro para o modelo correspondente. Quando o cliente chama **IClassFactory:: CreateInstance**, a fábrica de classes chama a função de instanciação definida no modelo.

para obter mais informações, consulte [como criar uma DLL de filtro de DirectShow](how-to-create-a-dll.md).



| Variáveis de membro público                                                   | Descrição                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**\_nome m**](cfactorytemplate-m-name.md)                                | Nome do filtro.                                                        |
| [**ClsID do m \_**](cfactorytemplate-m-clsid.md)                              | Ponteiro para o CLSID do objeto.                                        |
| [**\_lpfnNew m**](cfactorytemplate-m-lpfnnew.md)                          | Ponteiro para uma função que cria uma instância do objeto.              |
| [**\_lpfnInit m**](cfactorytemplate-m-lpfninit.md)                        | Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.           |
| [**\_filtro de pAMovieSetup m \_**](cfactorytemplate-m-pamoviesetup-filter.md) | Ponteiro para uma estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) . |
| Métodos públicos                                                            | Descrição                                                                |
| [**Isclassidid**](cfactorytemplate-isclassid.md)                           | Determina se um CLSID corresponde a este modelo de classe.                    |
| [**CreateInstance**](cfactorytemplate-createinstance.md)                 | Chama a função de criação de objeto para a classe.                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>combase. h (incluir Fluxos. h)</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib; </dt> <dt>Strmbasd. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de classe base](base-class-reference.md)
</dt> </dl>

 

