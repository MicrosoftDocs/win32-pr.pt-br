---
description: Etapa 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Etapa 1. Definir um mecanismo para definir a propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770063"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Etapa 1. Definir um mecanismo para definir a propriedade

O filtro deve dar suporte a uma maneira para a página de propriedades se comunicar com ela, para que a página de propriedades possa definir e recuperar propriedades no filtro. Os possíveis mecanismos incluem o seguinte:

-   Expor uma interface COM personalizada.
-   Suporte a propriedades de automação, por meio de **IDispatch**.
-   Expor a interface **IPropertyBag** e defina um conjunto de propriedades nomeadas.

Este exemplo usa uma interface COM personalizada, chamada ISaturation. Essa não é uma interface do DirectShow real; Ele é definido somente para este exemplo. Comece declarando a interface em um arquivo de cabeçalho, juntamente com o IID (identificador de interface):


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



Você também pode definir a interface com IDL e usar o compilador MIDL para criar o arquivo de cabeçalho. Em seguida, implemente a interface personalizada no filtro. Este exemplo usa os métodos "Get" e "set" para o valor de saturação do filtro. Observe que os dois métodos protegem o \_ membro m lSaturation com uma seção crítica.


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



É claro que os detalhes de sua própria implementação serão diferentes do exemplo mostrado aqui.

Em seguida: [etapa 2. Implemente ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



