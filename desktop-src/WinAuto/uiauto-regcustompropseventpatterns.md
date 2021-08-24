---
title: Registrar Propriedades personalizadas, eventos e padrões de controle
description: Antes que um padrão de propriedade, evento ou controle personalizado possa ser usado, o provedor e o cliente devem registrar a propriedade, o evento ou o padrão de controle em tempo de execução.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automação da interface do usuário, propriedades personalizadas
- Automação da interface do usuário, visão geral de eventos
- Visão geral da automação da interface do usuário, padrões de controle
- Automação da interface do usuário, registrando Propriedades personalizadas
- Automação da interface do usuário, registro de eventos
- Automação da interface do usuário, registro de padrões de controle
- Propriedades personalizadas, registrando
- eventos, registrando
- padrões de controle, registro
- registrando, propriedades personalizadas
- registrando, eventos
- registrando, padrões de controle
- padrões de controle, personalizado
- padrões de controle, implementando personalizados
- Implementando padrões de controle personalizados
- padrões de controle personalizados
- wrappers de cliente
- manipuladores de padrões
- Implementando manipuladores de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7205d088f76f235b3078d5a053202f3d39b609389ef6adbc5dbdbca18d9b652b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118564047"
---
# <a name="register-custom-properties-events-and-control-patterns"></a>Registrar Propriedades personalizadas, eventos e padrões de controle

Antes que um padrão de propriedade, evento ou controle personalizado possa ser usado, o provedor e o cliente devem registrar a propriedade, o evento ou o padrão de controle em tempo de execução. O registro é efetivo globalmente dentro de um processo de aplicativo e permanece em vigor até que o processo seja fechado ou o último objeto de elemento de automação da interface do usuário da Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) ou [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) seja liberado dentro do processo.

O registro envolve a passagem de um GUID para a automação da interface do usuário, juntamente com informações detalhadas sobre a propriedade personalizada, evento ou padrão de controle. A tentativa de registrar o mesmo GUID uma segunda vez com as mesmas informações terá êxito, mas tentar registrar o mesmo GUID uma segunda vez, mas com informações diferentes (por exemplo, uma propriedade personalizada de um tipo diferente) falhará. No futuro, se a especificação personalizada for aceita e integrada ao núcleo de automação da interface do usuário, a automação da interface do usuário validará as informações de registro personalizadas e usará o código já registrado em vez da implementação da estrutura "oficial", minimizando assim os problemas de compatibilidade do aplicativo. Você não pode remover propriedades, eventos ou padrões de controle que já estão registrados.

Este tópico contém as seguintes seções:

-   [Registrando Propriedades e eventos personalizados](#registering-custom-properties-and-events)
-   [Implementando padrões de controle personalizados](#implementing-custom-control-patterns)
    -   [O wrapper do cliente e o manipulador de padrão](#the-client-wrapper-and-the-pattern-handler)
    -   [Implementando o wrapper do cliente](#implementing-the-client-wrapper)
    -   [Implementando o manipulador de padrões](#implementing-the-pattern-handler)
    -   [Registrando um padrão de controle personalizado](#registering-a-custom-control-pattern)
    -   [Exemplo de implementação de um padrão de controle personalizado](#example-implementation-of-a-custom-control-pattern)
-   [Tópicos relacionados](#related-topics)

## <a name="registering-custom-properties-and-events"></a>Registrando Propriedades e eventos personalizados

O registro de uma propriedade ou evento personalizado permite que o provedor e o cliente obtenham uma ID para a propriedade ou evento, que pode ser passada para vários métodos de API que usam IDs como parâmetros.

Para registrar uma propriedade ou evento:

1.  Defina um GUID para a propriedade ou evento personalizado.
2.  Preencha uma estrutura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) com informações sobre a propriedade ou o evento, incluindo o GUID e uma cadeia de caracteres não localizável que contém o nome da propriedade ou do evento personalizado. As propriedades personalizadas também exigem que o tipo de dados da propriedade seja especificado, por exemplo, se a propriedade contém um inteiro ou uma cadeia de caracteres. O tipo de dados deve ser um dos tipos a seguir especificados pela enumeração [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Nenhum outro tipo de dados tem suporte para propriedades personalizadas.
    -   **\_Bool UIAutomationType**
    -   **UIAutomationType \_ duplo**
    -   **\_Elemento UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **Ponto de UIAutomationType \_**
    -   **\_Cadeia de caracteres UIAutomationType**
3.  Use a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperar um ponteiro para a interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) do objeto.
4.  Chame o método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) e passe o endereço da estrutura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou da estrutura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .

O método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) retorna uma ID de propriedade ou ID de evento que um aplicativo pode passar para qualquer método de automação de interface do usuário que usa um identificador como um parâmetro. Por exemplo, você pode passar uma ID de propriedade registrada para o método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) ou para o método [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .

O exemplo a seguir demonstra como registrar uma propriedade personalizada.


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



Os identificadores de propriedade e evento recuperados pelos métodos [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) e [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) são válidos somente no contexto do aplicativo que os recupera e apenas durante o tempo de vida do aplicativo. Os métodos de registro podem retornar valores inteiros diferentes para o mesmo GUID quando ele é chamado em instâncias de tempo de execução diferentes do mesmo aplicativo.

Não há nenhum método que cancele o registro de uma propriedade ou evento personalizado. Em vez disso, eles são implicitamente cancelados no registro quando o último objeto de automação da interface do usuário é liberado.

> [!IMPORTANT]
> Se o seu código for um cliente Microsoft Acessibilidade Ativa (MSAA), você deverá chamar a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) quando alterar o valor de uma propriedade personalizada.

 

## <a name="implementing-custom-control-patterns"></a>Implementando padrões de controle personalizados

Um padrão de controle personalizado não está incluído na API de automação da interface do usuário, mas é fornecido por terceiros em tempo de execução. Os desenvolvedores de aplicativos cliente e provedor devem trabalhar juntos para definir um padrão de controle personalizado, incluindo os métodos, as propriedades e os eventos que o padrão de controle dará suporte. Depois de definir o padrão de controle, o cliente e o provedor devem implementar o suporte a objetos Component Object Model (COM), juntamente com o código para registrar o padrão de controle em tempo de execução. Um padrão de controle personalizado requer a implementação de dois objetos COM: um wrapper de cliente e um manipulador de padrão.

> [!Note]  
> Os exemplos nos tópicos a seguir ilustram como implementar um padrão de controle personalizado que duplica a funcionalidade do padrão de controle de [valor](uiauto-implementingvalue.md) existente. Esses exemplos são apenas para fins de instrução. Um padrão de controle personalizado real deve fornecer funcionalidade que não está disponível nos padrões de controle de automação da interface do usuário padrão.

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a>O wrapper do cliente e o manipulador de padrão

O wrapper do cliente implementa a API que é usada pelo cliente para recuperar propriedades e métodos de chamada expostos pelo padrão de controle personalizado. A API é implementada como uma interface COM que passa todas as solicitações de propriedade e chamadas de método para o núcleo de automação da interface do usuário, que realiza marshaling das solicitações e chamadas para o provedor.

O código que registra um padrão de controle personalizado deve fornecer uma fábrica de classes que a automação da interface do usuário pode usar para criar instâncias do objeto de wrapper do cliente. Quando um padrão de controle personalizado é registrado com êxito, a automação da interface do usuário retorna um ponteiro de interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) que é usado pelo cliente para encaminhar solicitações de propriedade e chamadas de métodos para o núcleo de automação da interface do usuário.

No lado do provedor, o núcleo de automação da interface do usuário usa as solicitações de propriedade e chamadas de método do cliente e as passa para o objeto de manipulador de padrão. Em seguida, o manipulador de padrões chama os métodos apropriados na interface do provedor para o padrão de controle personalizado.

O código que registra um padrão de controle personalizado cria o objeto de manipulador de padrão e, ao registrar o padrão de controle, fornece automação de interface do usuário com um ponteiro para a interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto.

O diagrama a seguir mostra como uma solicitação de propriedade de cliente ou uma chamada de método flui do wrapper do cliente, por meio dos componentes principais de automação da interface do usuário para o manipulador de padrões e, em seguida, para a interface do provedor.

![diagrama mostrando o fluxo do wrapper do cliente para o manipulador de padrões e o provedor](images/custompatternsupport.jpg)

Os objetos que implementam as interfaces do manipulador de padrões e do wrapper do cliente devem ser de thread livre. Além disso, o núcleo de automação da interface do usuário deve ser capaz de chamar os objetos diretamente sem qualquer código de marshaling intermediário.

### <a name="implementing-the-client-wrapper"></a>Implementando o wrapper do cliente

O wrapper do cliente é um objeto que expõe uma interface IXxxPattern que o cliente usa para solicitar Propriedades e chamar métodos com suporte pelo padrão de controle personalizado. A interface consiste em um par de métodos "getter" para cada propriedade com suporte (get \_ CurrentXxx e get \_ CachedXxx Method) e um método "Caller" para cada método com suporte. Quando o objeto é instanciado, o construtor de objeto recebe um ponteiro para a interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , que é implementada pelo núcleo de automação da interface do usuário. Os métodos da interface IXxxPattern usam os métodos [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) e [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) para encaminhar solicitações de propriedade e chamadas de método para o núcleo de automação da interface do usuário.

O exemplo a seguir mostra como implementar um objeto de wrapper de cliente para um padrão de controle personalizado simples que dá suporte a uma única propriedade. Para obter um exemplo mais complexo, consulte [exemplo de implementação de um padrão de controle personalizado](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a>Implementando o manipulador de padrões

O manipulador de padrões é um objeto que implementa a interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) . Essa interface tem dois métodos: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) e [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch). O método **CreateClientWrapper** é chamado pelo núcleo de automação da interface do usuário e recebe um ponteiro para a interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) . **CreateClientWrapper** responde instanciando o objeto wrapper do cliente e passando o ponteiro de interface **IUIAutomationPatternInstance** para o construtor do wrapper do cliente.

O método de [**expedição**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) é usado pelo núcleo de automação da interface do usuário para passar solicitações de propriedade e chamadas de método para a interface do provedor para o padrão de controle personalizado. Os parâmetros incluem um ponteiro para a interface do provedor, o índice de base zero do getter de propriedade ou o método que está sendo chamado e uma matriz de estruturas [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) que contêm os parâmetros a serem passados para o provedor. O manipulador de padrões responde verificando o parâmetro de índice para determinar qual método de provedor deve ser chamado e, em seguida, chama essa interface de provedor, passando os parâmetros contidos nas estruturas **UIAutomationParameter** .

O objeto de manipulador de padrão é instanciado pelo mesmo código que registra o padrão de controle personalizado, antes de o padrão de controle ser registrado. O código deve passar o ponteiro de interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto de manipulador padrão para o núcleo de automação da interface do usuário no momento do registro.

O exemplo a seguir mostra como implementar um objeto de manipulador de padrão para um padrão de controle personalizado simples que dá suporte a uma única propriedade. Para obter um exemplo mais complexo, consulte [exemplo de implementação de um padrão de controle personalizado](#example-implementation-of-a-custom-control-pattern).


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a>Registrando um padrão de controle personalizado

Antes de poder ser usado, um padrão de controle personalizado deve ser registrado pelo provedor e pelo cliente. O registro fornece ao núcleo Automação da Interface do Usuário informações detalhadas sobre o padrão de controle e fornece ao provedor ou ao cliente a ID do padrão de controle e as IDs para as propriedades e eventos com suporte pelo padrão de controle. No lado do provedor, o padrão de controle personalizado deve ser registrado antes que o controle associado manipular a mensagem [**WM \_ GETOBJECT**](wm-getobject.md) ou ao mesmo tempo.

Ao registrar um padrão de controle personalizado, o provedor ou o cliente fornece as seguintes informações:

-   O GUID do padrão de controle personalizado.
-   Uma cadeia de caracteres não localizável que contém o nome do padrão de controle personalizado.
-   O GUID da interface do provedor que dá suporte ao padrão de controle personalizado.
-   O GUID da interface do cliente que dá suporte ao padrão de controle personalizado.
-   Uma matriz de [**estruturas UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) que descrevem as propriedades com suporte pelo padrão de controle personalizado. Para cada propriedade, o GUID, o nome da propriedade e o tipo de dados devem ser especificados.
-   Uma matriz de [**estruturas UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) que descrevem os métodos com suporte pelo padrão de controle personalizado. Para cada método, a estrutura inclui as seguintes informações: o nome do método, uma contagem de parâmetros, uma lista de tipos de dados de parâmetro e uma lista dos nomes de parâmetro.
-   Uma matriz de [**estruturas UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) que descrevem os eventos gerados pelo padrão de controle personalizado. Para cada evento, o GUID e o nome do evento devem ser especificados.
-   O endereço da interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto do manipulador de padrões que disponibiliza o padrão de controle personalizado para os clientes.

Para registrar o padrão de controle personalizado, o provedor ou o código do cliente deve executar as seguintes etapas:

1.  Preencha uma [**estrutura UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) com as informações anteriores.
2.  Use a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperar um ponteiro para a interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) do objeto.
3.  Chame o [**método IUIAutomationRegistrar::RegisterPattern,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) passando o endereço da estrutura [**UIAutomationPatternInfo.**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)

O [**método RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) retorna uma ID de padrão de controle, juntamente com uma lista de IDs de propriedade e IDs de evento. Um aplicativo pode passar essas IDs para qualquer Automação da Interface do Usuário que aceita esse identificador como um parâmetro. Por exemplo, você pode passar uma ID de padrão registrada para o método [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) para recuperar um ponteiro para a interface do provedor para o padrão de controle.

Não há nenhum método que não registro um padrão de controle personalizado. Em vez disso, ele é implicitamente não registro quando o último objeto Automação da Interface do Usuário é liberado.

Para ver um exemplo que mostra como registrar um padrão de controle personalizado, consulte a seção a seguir.

### <a name="example-implementation-of-a-custom-control-pattern"></a>Exemplo de implementação de um padrão de controle personalizado

Esta seção contém um código de exemplo que demonstra como implementar o wrapper do cliente e objetos de manipulador de padrões para um padrão de controle personalizado. O exemplo implementa um padrão de controle personalizado baseado no padrão [de controle](uiauto-implementingvalue.md) Value.


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Projetando propriedades, eventos e padrões de controle personalizados](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 