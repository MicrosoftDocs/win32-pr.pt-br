---
description: Se ocorrer um erro, o WMI retornará um código de erro como um valor HRESULT. Esses códigos podem ser retornados por scripts, aplicativos C++ ou WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes de erro de WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791441"
---
# <a name="wmi-error-constants"></a>Constantes de erro WMI

Se ocorrer um erro, o WMI retornará um código de erro como um valor **HRESULT** . Esses códigos podem ser retornados por scripts, aplicativos C++ ou [**WMIC**](wmic.md).

> [!Note]
>
> A documentação a seguir destina-se a desenvolvedores e administradores de ti. Se você for um usuário final que recebeu uma mensagem de erro relacionada ao WMI, vá para [suporte da Microsoft](https://support.microsoft.com/) e procure o código de erro que você vê na mensagem de erro. Para obter mais informações sobre como solucionar problemas com scripts WMI e o serviço WMI, consulte o [WMI não está funcionando!](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI. As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI. Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.
>
> Para obter mais informações sobre a origem do problema, você pode baixar e executar a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo. O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo. Você pode baixar o Utilitário de Diagnóstico WMI [aqui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo). Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando. Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.

A lista a seguir lista alguns intervalos de erros comuns.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099
</dt> <dd>

Erros originados no próprio WMI.

Uma operação WMI específica falhou devido a

-   Um erro na solicitação, por exemplo, uma consulta WQL falha ou a conta não tem as permissões corretas.
-   Um problema de infraestrutura do WMI, como registro incorreto de CIM ou DCOM.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Erros originados no sistema operacional principal. O WMI pode retornar esse tipo de erro devido a uma falha externa, por exemplo, falha de segurança DCOM.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Erros originados no DCOM. Por exemplo, a configuração de DCOM para operações em um computador remoto pode estar incorreta.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Erro originado de ADSI (Active Directory interfaces de serviço) ou LDAP (Lightweight Directory Access Protocol), por exemplo, uma falha de acesso de Active Directory ao usar os provedores de Active Directory do WMI.

</dd> </dl>

Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo). Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando. Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível. Em C++, você pode chamar [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e especificar **C: \\ Windows \\ System32 \\ WBEM \\wmiutils.dll** como o módulo de mensagem.

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**falha de WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Falha na chamada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Objeto não encontrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**acesso ao WBEM \_ E \_ \_ negado**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



O usuário atual não tem permissão para executar a ação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_falha do \_ provedor WBEM E \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



O provedor falhou em algum momento diferente durante a inicialização.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilidade de \_ tipo WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Erro de incompatibilidade de tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ memória insuficiente \_ \_**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Não há memória suficiente para a operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ contexto inválido do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



O objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) não é válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**parâmetro de WBEM \_ E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Um dos parâmetros para a chamada não está correto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ não \_ disponível**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



O recurso, normalmente um servidor remoto, não está disponível no momento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_ \_ erro crítico de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Ocorreu um erro interno, crítico e inesperado. Relate o erro ao suporte técnico da Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ fluxo inválido do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



Um ou mais pacotes de rede foram corrompidos durante uma sessão remota.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ não \_ há suporte para o WBEM E**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Não há suporte para o recurso ou operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**superclasse WBEM \_ E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



A classe pai especificada não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ \_ namespace inválido**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



O namespace especificado não pode ser encontrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_objeto WBEM E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



A instância especificada não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_classe WBEM E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



A classe especificada não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_provedor WBEM \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



O provedor referenciado no esquema não tem um registro correspondente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM \_ E \_ \_ registro de provedor inválido \_**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



O provedor referenciado no esquema tem um registro incorreto ou incompleto.

Esse erro pode ser causado por muitas condições, incluindo as seguintes:

-   Um comando de [ \# namespace de pragma](pragma-namespace.md) ausente no arquivo de formato MOF (MOF) usado para registrar o provedor. O provedor pode ser registrado no namespace WMI errado.
-   Falha ao recuperar o registro COM.
-   O modelo de hospedagem não é válido. Para obter mais informações, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).
-   Uma classe especificada no registro não é válida.
-   Falha ao criar uma instância do ou herdar da classe [**\_ \_ Win32Provider**](--win32provider.md) para criar o registro do provedor no arquivo MOF.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_falha de \_ carregamento do provedor WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM não pode localizar um provedor referenciado no esquema.

Esse erro pode ser causado por muitas condições, incluindo as seguintes:

-   O provedor está usando uma DLL WMI que não corresponde ao arquivo. lib usado quando o provedor foi criado.
-   A DLL do provedor, ou qualquer uma das DLLs das quais ela depende, está corrompida.
-   Falha do provedor ao exportar [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).
-   O provedor em processo não foi registrado usando o comando **regsvr32** .
-   O provedor fora do processo não foi registrado usando a opção **/RegServer** . Por exemplo, **myprog.exe/RegServer**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ falha na inicialização do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



O componente, como um provedor, não pôde ser inicializado por motivos internos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_falha de \_ transporte \_ E de WBEM**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Erro de rede que impede que a operação normal ocorra.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**operação de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



A operação solicitada não é válida. Esse erro geralmente se aplica a tentativas inválidas para excluir classes ou propriedades.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ consulta inválida \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



A consulta não era sintaticamente válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Não há suporte para a linguagem de consulta solicitada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**o WBEM \_ E \_ já \_ existe**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



Em uma operação put, o sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**substituição de WBEM \_ E \_ \_ não \_ permitida**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



Não é possível executar a operação de adição neste qualificador porque o objeto proprietário não permite substituições.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_qualificador do WBEM E \_ propagado \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



O usuário tentou excluir um qualificador que não era de propriedade. O qualificador foi herdado de uma classe pai.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**Propriedade de WBEM \_ E \_ propagada \_**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



O usuário tentou excluir uma propriedade que não era de propriedade. A propriedade foi herdada de uma classe pai.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ inesperado**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



O cliente fez uma sequência de chamadas inesperada e ilegal, como chamar [**Endenumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) antes de chamar [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**operação de WBEM \_ E \_ ilegal \_**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



O usuário solicitou uma operação ilegal, como a geração de uma classe de uma instância.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ não podem \_ ser \_ chave**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Tentativa inválida de especificar um qualificador de chave em uma propriedade que não pode ser uma chave. As chaves são especificadas na definição de classe para um objeto e não podem ser alteradas por instância.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_classe WBEM E \_ incompleta \_**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



O objeto atual não é uma definição de classe válida. Ele está incompleto ou não foi registrado com WMI usando [**SWbemObject. put \_**](swbemobject-put-.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**sintaxe de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



A consulta é sintaticamente inválida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_objeto WBEM E não \_ decorado \_**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ somente leitura**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Foi feita uma tentativa de modificar uma propriedade somente leitura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_provedor WBEM \_ E \_ não \_ compatível**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



O provedor não pode executar a operação solicitada. Isso pode incluir uma consulta que seja muito complexa, recuperando uma instância, criando ou atualizando uma classe, excluindo uma classe ou enumerando uma classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**a \_ classe WBEM E \_ \_ tem \_ filhos**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Foi feita uma tentativa de fazer uma alteração que invalida uma subclasse.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**\_classe WBEM \_ E \_ possui \_ instâncias**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Foi feita uma tentativa de excluir ou modificar uma classe que tem instâncias.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_consulta WBEM \_ E \_ não \_ implementada**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ \_ nulo inválido**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



O valor de Nothing/**NULL** foi especificado para uma propriedade que deve ter um valor, como um que é marcado por um qualificador de [**chave**](key-qualifier.md), [**indexado**](optional-qualifiers.md)ou **não \_ nulo** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_tipo de \_ \_ qualificador E inválido \_ do WBEM**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Foi fornecido um valor de variante para um qualificador que não é um tipo de qualificador legal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**tipo de propriedade de WBEM \_ E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



O tipo CIM especificado para uma propriedade não é válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ valor \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



A solicitação foi feita com um valor fora do intervalo ou é incompatível com o tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ não podem \_ ser \_ singleton**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



Foi feita uma tentativa ilegal de tornar uma classe singleton, como quando a classe é derivada de uma classe não singleton.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ tipo CIM \_ inválido**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



O tipo CIM especificado não é válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ método inválido do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



O método solicitado não está disponível.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parâmetros de \_ \_ método inválido E WBEM \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Os parâmetros fornecidos para o método não são válidos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_Propriedade do \_ sistema WBEM E \_**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Houve uma tentativa de obter qualificadores em uma propriedade do sistema.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**Propriedade de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



O tipo de propriedade não é reconhecido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**chamada de WBEM \_ E \_ \_ cancelada**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



O processo assíncrono foi cancelado internamente ou pelo usuário. Observe que, devido ao tempo e à natureza da operação assíncrona, a operação pode não ter sido realmente cancelada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ desligando \_**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



O usuário solicitou uma operação enquanto o WMI está em processo de desligamento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ método propagado do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Foi feita uma tentativa de reutilizar um nome de método existente de uma classe pai e as assinaturas não coincidem.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**parâmetro de WBEM \_ E \_ sem suporte \_**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Um ou mais valores de parâmetro, como um texto de consulta, são muito complexos ou não têm suporte. Portanto, o WMI é solicitado a repetir a operação com parâmetros mais simples.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ID de \_ \_ parâmetro ausente \_ do WBEM E**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



O parâmetro estava ausente da chamada do método.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**ID de parâmetro de WBEM \_ E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



O parâmetro do método tem um qualificador de [**ID**](standard-wmi-qualifiers.md) que não é válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_IDs de parâmetro WBEM E não \_ consecutivo \_ \_**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Um ou mais dos parâmetros de método têm qualificadores de [**ID**](standard-wmi-qualifiers.md) fora de sequência.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID do parâmetro WBEM E \_ \_ no \_ RETVAL**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



O valor de retorno para um método tem um qualificador de [**ID**](standard-wmi-qualifiers.md) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**caminho de objeto do WBEM \_ E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



O caminho do objeto especificado não era válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ sem \_ \_ \_ espaço em disco**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



O disco está sem espaço ou o limite de 4 GB no repositório do WMI (repositório CIM) foi atingido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**o buffer do WBEM E o é \_ \_ \_ muito \_ pequeno**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



O buffer fornecido era muito pequeno para conter todos os objetos no enumerador ou para ler uma propriedade de cadeia de caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_extensão de \_ Put E sem \_ suporte \_ do WBEM**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



O provedor não oferece suporte à operação Put solicitada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_tipo de objeto WBEM E \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



O objeto com um tipo ou versão incorreto foi encontrado durante o marshaling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_tipo de pacote WBEM E \_ desconhecido \_ \_**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



Um pacote com tipo ou versão incorreta foi encontrado durante o marshaling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**incompatibilidade de versão do WBEM \_ E \_ Marshal \_ \_**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



O pacote tem uma versão sem suporte.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**assinatura de WBEM \_ E \_ Marshal \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



O pacote parece estar corrompido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_qualificador do WBEM E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Foi feita uma tentativa de qualificadores incompatíveis, como \[ colocar \] a chave em um objeto em vez de uma propriedade.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ \_ parâmetro duplicado WBEM E inválido \_**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



Parâmetro duplicado foi declarado em um método CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ muito \_ \_ dados**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E \_ servidor \_ muito \_ ocupado**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



Falha na chamada para [**IWbemObjectSink:: indication**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . O provedor pode acionar o evento novamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**tipo de WBEM \_ E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



O tipo qualificador especificado não era válido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ referência circular E de WBEM \_**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Foi feita uma tentativa de criar uma referência que é circular (por exemplo, derivando uma classe a partir dela).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_atualização de classe WBEM E \_ sem suporte \_ \_**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



Não há suporte para a classe especificada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ não pode \_ alterar a \_ herança de chave \_**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Foi feita uma tentativa de alterar uma chave quando instâncias ou subclasses já estão usando a chave.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ não é possível \_ alterar a \_ herança do índice \_**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Foi feita uma tentativa de alterar um índice quando instâncias ou subclasses já estão usando o índice.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ \_ muitas \_ Propriedades**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Foi feita uma tentativa de criar mais propriedades do que a versão atual da classe dá suporte.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**incompatibilidade de tipo de atualização WBEM \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



A propriedade foi redefinida com um tipo conflitante em uma classe derivada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**substituição de atualização de WBEM \_ E \_ \_ \_ não \_ permitida**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Foi feita uma tentativa em uma classe derivada para substituir um qualificador que não pode ser substituído.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_ \_ \_ método propagado de atualização de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



O método foi declarado novamente com uma assinatura conflitante em uma classe derivada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_método WBEM \_ E \_ não \_ implementado**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Foi feita uma tentativa de executar um método não marcado com \[ implementado \] em nenhuma classe relevante.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_método WBEM \_ E \_ desabilitado**
</dt> <dd> <dl> <dt>


</dt> <dt>



Foi feita uma tentativa de executar um método marcado com \[ desabilitado \] .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_ \_ atualizador de WBEM E \_ ocupado**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



O atualizador está ocupado com outra operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_consulta WBEM E não \_ analisável \_**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



A consulta de filtragem é sintaticamente inválida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**\_classe de evento WBEM E \_ not \_ \_**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



A cláusula FROM de uma consulta de filtragem faz referência a uma classe que não é uma classe de evento (não derivada do [**\_ \_ evento**](--event.md)).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ faltando \_ grupo \_ dentro de**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



Uma cláusula GROUP BY foi usada sem a cláusula GROUP WITHIN correspondente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ \_ lista de agregação ausente \_**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



Uma cláusula GROUP BY foi usada. Não há suporte para a agregação em todas as propriedades.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**\_ \_ a propriedade WBEM E \_ não \_ um \_ objeto**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



A notação de ponto foi usada em uma propriedade que não é um objeto inserido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ agregando \_ por \_ objeto**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Uma cláusula GROUP BY faz referência a uma propriedade que é um objeto inserido sem usar a notação de ponto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_consulta de provedor WBEM E não \_ interpretável \_ \_**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



A consulta de registro do provedor de eventos ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) não especificou as classes para as quais os eventos foram fornecidos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**\_execução da \_ \_ restauração de \_ backup \_ do WBEM E**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



Foi feita uma solicitação para fazer backup ou restaurar o repositório enquanto ele estava em uso pelo WinMgmt.exe ou pelo processo SVCHOST que contém o serviço WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**\_estouro de \_ fila WBEM E \_**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



A fila de entrega assíncrona estourou do consumidor de eventos está muito lenta.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ E \_ privilégio \_ não \_ mantidos**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



Falha na operação porque o cliente não tinha o privilégio de segurança necessário.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_ \_ operador inválido do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



O operador não é válido para este tipo de propriedade.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ credenciais locais do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



O usuário especificou nome de usuário/senha/autoridade em uma conexão local. O usuário deve usar um nome de usuário/senha em branco e contar com a segurança padrão.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ não podem \_ ser \_ abstratos**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



A classe tornou-se abstrata quando sua classe pai não é abstrata.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**\_objeto de \_ emendado E de WBEM \_**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



O objeto emendado foi gravado sem o **sinalizador WBEM usar sinalizador de \_ \_ \_ \_ qualificadores corrigidos** sendo especificado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_cliente WBEM E/s \_ \_ muito \_ lento**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



O cliente não recuperou objetos com rapidez suficiente a partir de uma enumeração. Essa constante é retornada quando um cliente cria um objeto de enumeração, mas não recupera objetos do enumerador em tempo hábil, fazendo com que os caches do objeto do enumerador sejam armazenados em backup.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**\_ \_ \_ descritor de segurança de WBEM E nulo \_**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



Foi usado um descritor de segurança nulo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM \_ E \_ atingiu o tempo \_ limite**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



Tempo limite da operação atingido.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**Associação de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



A associação não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**operação de WBEM \_ E \_ ambígua \_**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



A operação era ambígua.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violação de \_ cota \_ E de WBEM**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



O WMI está ocupando muita memória. Isso pode ser causado por baixa disponibilidade de memória ou consumo excessivo de memória pelo WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflito de \_ Transações WBEM E \_**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



A operação resultou em um conflito de transação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**reversão do WBEM \_ E \_ forçada \_**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



A transação forçou uma reversão.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**localidade do WBEM \_ E \_ sem suporte \_**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



Não há suporte para a localidade usada na chamada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**\_ \_ identificador de WBEM E \_ desatualizado \_ \_**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



O identificador de objeto está desatualizado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**\_ \_ falha na conexão do WBEM E \_**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Falha na conexão com o banco de dados SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_solicitação de \_ \_ identificador inválido \_ do WBEM E**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



A solicitação de identificador não era válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nome da propriedade WBEM E \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



O nome da propriedade contém mais de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_nome de classe WBEM E \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



O nome da classe contém mais de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**\_nome do método WBEM E \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



O nome do método contém mais de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**o \_ nome do qualificador E do WBEM é \_ \_ \_ muito \_ grande**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



O nome do qualificador contém mais de 255 caracteres.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM \_ E \_ executar novamente o \_ comando**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



O comando SQL deve ser executado novamente porque há um deadlock no SQL. Isso pode ser retornado somente quando os dados estão sendo armazenados em um banco de dado SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**incompatibilidade de \_ versão do banco de dados WBEM E \_ \_ \_**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



A versão do banco de dados não corresponde à versão que o driver do repositório processa.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**exclusão de WBEM \_ E \_ veta \_**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



O WMI não pode executar a operação de exclusão porque o provedor não permite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ vetar \_ put**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



O WMI não pode executar a operação Put porque o provedor não permite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ localidade inválida do WBEM E \_**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



O identificador de localidade especificado não era válido para a operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_provedor WBEM \_ E \_ suspenso**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



O provedor está suspenso.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**sincronização de WBEM \_ E \_ \_ necessária**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



O objeto deve ser gravado no repositório WMI e recuperado novamente para que a operação solicitada possa ser realizada com sucesso. Essa constante é retornada quando um objeto deve ser confirmado e recuperado para ver o valor da propriedade.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ sem \_ esquema**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



A operação não pode ser concluída; nenhum esquema está disponível.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**\_provedor WBEM \_ E \_ já \_ registrado**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



O provedor não pode ser registrado porque já está registrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_provedor WBEM \_ E \_ não \_ registrado**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



O provedor não foi registrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_erro de \_ \_ transporte fatal \_ de WBEM E**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Ocorreu um erro de transporte fatal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**conexão de WBEM \_ E \_ criptografada \_ \_ necessária**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



O usuário tentou definir um nome de computador ou domínio sem uma conexão criptografada.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**o \_ provedor WBEM E \_ \_ atingiu o tempo \_ limite**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Um provedor não pôde relatar resultados dentro do tempo limite especificado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**\_ \_ nenhuma \_ chave do WBEM E**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



O usuário tentou colocar uma instância sem chave definida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_provedor WBEM \_ E \_ desabilitado**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



O usuário tentou registrar uma instância do provedor, mas o servidor COM da instância do provedor foi descarregado.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS \_ E \_ registro \_ muito \_ amplo**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



O registro do provedor se sobrepõe ao domínio de evento do sistema.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS \_ E \_ registro \_ muito \_ preciso**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



Uma cláusula WITHIN não foi usada nesta consulta.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ AUTHZ \_ não \_ privilegiado**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Este computador não tem as permissões de domínio necessárias para dar suporte às funções de segurança relacionadas à instância de assinatura criada. Contate o administrador de domínio para que este computador seja adicionado ao grupo de acesso de autorização do Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E \_ tentar novamente \_ mais tarde**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**contenção de \_ recurso WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ nome do qualificador esperado \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Esperado um nome de qualificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ \_ semi esperado**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Ponto-e-vírgula esperado ou ' = '.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ chave de abertura esperada \_**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Chave de abertura esperada.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ chave de fechamento esperada \_**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Chave de fechamento ausente ou elemento de matriz inválido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ colchete de fechamento esperado \_**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Esperado um colchete de fechamento.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parêntese de fechamento esperado \_**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Parêntese de fechamento esperado.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valor constante \_ ilegal**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Valor numérico fora do intervalo ou cadeias de caracteres sem aspas.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificador de tipo esperado \_**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Esperado um identificador de tipo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ esperado \_ abrir \_ parênteses**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Esperado um parêntese de abertura.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**\_token WBEMMOF E \_ não reconhecido \_**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Token inesperado no arquivo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ tipo não reconhecido \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Identificador de tipo não reconhecido ou sem suporte.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ \_ nome da propriedade esperado \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Propriedade ou nome de método esperado.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**\_ \_ \_ não \_ há suporte para WBEMMOF E TYPEDEF**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



Não há suporte para TYPEDEFs e tipos enumerados.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ alias inesperado \_**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Somente uma referência a um objeto de classe pode ter um valor de alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ \_ inicialização de matriz inesperada \_**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Inicialização de matriz inesperada. As matrizes devem ser declaradas com \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de emenda inválida \_**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



A sintaxe do caminho do namespace não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ alteração de duplicação inválida \_**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Duplicar especificadores de emenda.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ \_ pragma inválido**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



[ \# pragma](pragma-namespace.md) deve ser seguido por uma palavra-chave válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de namespace inválida \_**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



A sintaxe do caminho do namespace não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ \_ nome de classe esperado \_**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



O caractere inesperado no nome da classe deve ser um identificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**incompatibilidade de \_ tipo E WBEMMOF \_ \_**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



O valor especificado não pode ser feito no tipo apropriado.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nome de alias esperado \_**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



Cifrão deve ser seguido por um nome de alias como um identificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ declaração de classe inválida \_**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



Declaração de classe inválida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ declaração de instância inválida \_**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



A declaração de instância não é válida. Ele deve começar com "instance of"


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dólar esperado**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Sinal de dólar esperado. Um alias no formato "$name" deve seguir a palavra-chave "as".


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_ \_ qualificador WBEMMOF E CimType \_**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



O qualificador "CIMTYPE" não pode ser especificado diretamente em um arquivo MOF. Use a notação de tipo padrão.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ duplicar \_ Propriedade**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



Nome de propriedade duplicado encontrado no MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ \_ especificação de namespace inválido \_**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



A sintaxe do namespace não é válida. Referências a outros servidores não são permitidas.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Valor fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E \_ \_ arquivo inválido**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



O arquivo não é um arquivo MOF de texto válido ou arquivo MOF binário.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF \_ E \_ aliases \_ no \_ Embedded**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Objetos inseridos não podem ser aliases.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**\_matriz WBEMMOF \_ E \_ \_ elem nula**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



Não há suporte para elementos nulos em uma matriz.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**\_ \_ qualificador WBEMMOF E duplicado \_**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



O qualificador foi usado mais de uma vez no objeto.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ tipo de flavor esperado \_**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Era esperado um tipo de flavor como **ToInstance**, **ToSubClass**, **EnableOverride** ou **DisableOverride**.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**\_tipos de \_ tipo incompatíveis E \_ WBEMMOF \_**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



A combinação de **EnableOverride** e **DisableOverride** no mesmo qualificador não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ vários \_ aliases**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Um alias não pode ser usado duas vezes.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**\_ \_ \_ Tipo TYPES2 WBEMMOF E incompatível \_**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



A combinação de **Restricted** e **ToInstance** ou **ToSubClass** não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ nenhuma \_ matriz \_ retornada**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Os métodos não podem retornar valores de matriz.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ deve \_ estar \_ dentro \_ ou \_ fora**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Os argumentos devem ter um qualificador **de entrada** ou **saída** .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de sinalizadores inválidos \_**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



A sintaxe de sinalizadores não é válida.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ chave esperada \_ \_ ou \_ tipo inadequado \_**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



A chave final e o ponto-e-vírgula para uma classe estão ausentes.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ \_ \_ valor CIMV22 igual sem suporte \_**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



Não há suporte para um recurso de CIM versão 2,2 para um valor de qualificador.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**\_Tipo de \_ \_ dados CIMV22 WBEMMOF E sem suporte \_ \_**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



Não há suporte para o tipo de dados CIM versão 2,2.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**\_sintaxe de DELETEINSTANCE WBEMMOF E \_ inválida \_ \_**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



A sintaxe da instância de exclusão não é válida. Deve ser `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe de qualificador inválida \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



A sintaxe do qualificador não é válida. Ela deverá ser `qualifiername:type=value,scope(class|instance), flavorname`.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_ \_ qualificador WBEMMOF E \_ usado fora do \_ \_ escopo**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



O qualificador é usado fora de seu escopo.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ erro \_ ao \_ criar \_ arquivo temporário**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Erro ao criar arquivo temporário. O arquivo temporário é um estágio intermediário na compilação do MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF \_ E \_ erro \_ de \_ inclusão inválido de \_ arquivo**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Um arquivo incluído no MOF pelo comando de pré-processador [ \# include](-include.md) não é válido.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ sintaxe DELETECLASS inválida \_**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



A sintaxe para os comandos de pré-processador [ \# pragma deleteinstance](pragma-deleteinstance.md) ou [ \# pragma DeleteClass](pragma-deleteclass.md) não é válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de retorno do WMI](wmi-return-codes.md)
</dt> </dl>

 

