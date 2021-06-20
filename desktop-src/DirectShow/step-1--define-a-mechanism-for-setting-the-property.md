---
description: Defina um mecanismo para definir a propriedade como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Etapa 1. Definir um mecanismo para definir a propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 191014c35e27974c52961c2c6218e3a83effcc99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410069"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Etapa 1. Definir um mecanismo para definir a propriedade

O filtro deve dar suporte a uma maneira de a página de propriedades se comunicar com ele, para que a página de propriedades possa definir e recuperar propriedades no filtro. Os mecanismos possíveis incluem o seguinte:

-   Expor uma interface COM personalizada.
-   Suporte a propriedades de Automação, por **meio de IDispatch.**
-   Exponha a interface **IPropertyBag** e defina um conjunto de propriedades nomeadas.

Este exemplo usa uma interface COM personalizada, chamada IS saturação. Essa não é uma interface real do DirectShow; ele é definido somente para este exemplo. Comece declarando a interface em um arquivo de header, juntamente com o IID (identificador de interface):


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



Você também pode definir a interface com IDL e usar o compilador MIDL para criar o arquivo de header. Em seguida, implemente a interface personalizada no filtro. Este exemplo usa os métodos "Get" e "Set" para o valor de saturação do filtro. Observe que ambos os métodos protegem o membro m \_ lSaturation com uma seção crítica.


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

Próximo: [Etapa 2. Implemente ISpecifyPropertyPages.](step-2--implement-ispecifypropertypages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



