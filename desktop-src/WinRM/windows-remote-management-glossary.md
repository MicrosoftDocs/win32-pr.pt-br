---
title: Windows Glossário de Gerenciamento Remoto
description: Página do glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532562a45090040cebbefae2bfff601727efb8bca794a9d9833e61a53ad63a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743258"
---
# <a name="windows-remote-management-glossary"></a>Windows Glossário de Gerenciamento Remoto


<dl> <dt>

wsman:Items****
</dt> <dd>

Um WS-Management de protocolo retornado em uma enumeração que obtém as instâncias e os [*EPRs da instância*](/windows). **wsman:Items é** um contêiner que contém uma instância e sua EPR. Esse tipo de enumeração é iniciado quando o **sinalizador WSManFlagReturnObjectAndEPR** é definido na solicitação.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**controlador de gerenciamento de placa base (BMC)**
</dt> <dd>

Um microcontrolador anexado localmente a um servidor. Os BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo se o servidor estiver offline. Você tem acesso aos dados do BMC por meio do provedor WMI da INTERFACE de Gerenciamento de Plataforma Inteligente [*(IPMI).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticação Básica**
</dt> <dd>

O nome de usuário e a senha enviados na troca de autenticação. A autenticação básica pode ser configurada para usar o transporte HTTP ou HTTPS em um domínio ou grupo de trabalho. Esse método é o método menos seguro de autenticação.

</dd> <dt>

**BMC**
</dt> <dd>

Consulte [*controlador de gerenciamento de placa base (BMC).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Cim**
</dt> <dd>

Consulte [*modelo CIM (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

O aplicativo cliente usando o protocolo WS-Management para acessar o serviço de gerenciamento no computador local ou remoto.

</dd> <dt>

**CIM (Modelo de Informação Comum)**
</dt> <dd>

O [*modelo DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) que descreve como representar objetos de rede e computador do mundo real. O CIM usa um paradigma orientado a objeto, em que os objetos gerenciados são modelados usando os conceitos de classes e instâncias.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Autenticação Digest**
</dt> <dd>

Uma troca na qual o servidor recebe uma solicitação de um cliente e envia dados sobre o cliente para um servidor de autenticação, normalmente um controlador de domínio. Se o cliente for autenticado, o servidor receberá uma chave de sessão Digest usada para autenticar as solicitações subsequentes do cliente.

</dd> <dt>

**DMTF (Distributed Management Task Force)**
</dt> <dd>

A organização do setor que desenvolve padrões de gerenciamento e tecnologia de integração para ambientes corporativos e de Internet.

</dd> <dt>

**Dmtf**
</dt> <dd>

Consulte [*DMTF (Distributed Management Task Force).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Um recurso que pode ser resolvido por uma [*EPR (referência de*](windows-remote-management-glossary.md)ponto de extremidade).

</dd> <dt>

**referência de ponto de extremidade (EPR)**
</dt> <dd>

Uma combinação de WS-Addressing e WS-Management que juntos descrevem um endereço para um recurso no header SOAP da mensagem. Esse é um termo de serviço Web.

</dd> <dt>

**enumeração**
</dt> <dd>

Um conjunto ou coleção de instâncias [*de*](windows-remote-management-glossary.md) recurso ou a ação de solicitar esse conjunto. No WS-Management protocolo, [*o WS-Enumeration*](windows-remote-management-glossary.md) é usado para obter a coleção. Na implementação de script do serviço WinRM de enumeração, [**Session.Enumerate**](session-enumerate.md) e o [**objeto Enumerator**](enumerator.md) são usados. O método e a interface C++ [**correspondentes são IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Consulte [*EPR (referência de ponto de extremidade).*](windows-remote-management-glossary.md)

</dd> <dt>

**Serviço de Coleta de Eventos**
</dt> <dd>

O componente do sistema operacional que recebe eventos do BMC e de outros componentes ou aplicativos do sistema operacional.

</dd> <dt>

**encaminhamento de eventos**
</dt> <dd>

Uma notificação de eventos que ocorrem em computadores remotos pode ser enviada para aplicativos de assinatura. O encaminhamento de eventos não é um recurso do WinRM, mas do [log de Windows eventos](/windows/desktop/WES/windows-event-log). O encaminhamento de eventos fica disponível pela primeira vez no Windows Vista. Os aplicativos de gerenciamento, como o MOM (Microsoft Operations Manager) usam o encaminhamento de eventos.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Um mecanismo de consulta para especificar um conjunto limitado de instâncias na solicitação de um [*recurso*](windows-remote-management-glossary.md). Você pode especificar um *parâmetro de* filtro em chamadas [**para Session.Enumerate**](session-enumerate.md) ou [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

**dialeto de filtro**
</dt> <dd>

Uma cadeia de caracteres XML que [](windows-remote-management-glossary.md) identifica o dialeto XML usado para especificar um filtro em uma chamada para [**Session.Enumerate**](session-enumerate.md) ou [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate). O serviço WinRM dá suporte [ao WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) como um dialeto de filtro ao receber solicitações.

</dd> <dt>

**Fragmento**
</dt> <dd>

Uma cadeia de caracteres XML que identifica parte de uma instância de um recurso em vez de todo o recurso. O suporte a fragmentos é encontrado [**no objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**dialeto de fragmento**
</dt> <dd>

Uma cadeia de caracteres XML que identifica o dialeto XML usado para especificar um [*fragmento*](windows-remote-management-glossary.md). O suporte a fragmentos é encontrado [**no objeto ResourceLocator.**](resourcelocator.md) O serviço WinRM dá suporte [*a XPath para*](windows-remote-management-glossary.md) dialeto de fragmento ao receber solicitações.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**in-band**
</dt> <dd>

O aplicativo cliente obtém dados BMC por meio do [*ouvinte*](windows-remote-management-glossary.md) WinRM no sistema operacional.

</dd> <dt>

**IPMI (Interface de Gerenciamento de Plataforma Inteligente)**
</dt> <dd>

Um padrão do setor de TI para a arquitetura do [*BMC (controlador de gerenciamento*](windows-remote-management-glossary.md)de placa base). Os Windows de gerenciamento de hardware fornecem um [*driver IPMI*](windows-remote-management-glossary.md) e um provedor [*IPMI*](windows-remote-management-glossary.md) WMI que permitem que scripts de gerenciamento, ferramentas de linha de comando e aplicativos obtenham dados do BMC. O provedor IPMI tem classes [WMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

</dd> <dt>

**IPMI**
</dt> <dd>

Consulte [*Interface de Gerenciamento de Plataforma Inteligente (IMPI)*](windows-remote-management-glossary.md).

</dd> <dt>

**Driver IPMI**
</dt> <dd>

O driver de kernel que permite o acesso a dispositivos [*BMC (controlador*](windows-remote-management-glossary.md) de gerenciamento de placa base) dos componentes do sistema operacional.

</dd> <dt>

**Provedor IPMI**
</dt> <dd>

Um provedor WMI padrão que define classes que modelam o [*IPMI*](windows-remote-management-glossary.md) e seus dados. O [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) é uma DLL COM que obtém dados do BMC.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Consulte [*Estilo do controlador de teclado (KCS).*](windows-remote-management-glossary.md)

</dd> <dt>

**Autenticação Kerberos**
</dt> <dd>

Um método de autenticação mútua entre o cliente e o servidor que usa chaves criptografadas. Para computadores em execução Windows sistema operacional baseado em Windows, a conta de cliente deve ser uma conta de domínio no mesmo domínio que o servidor. Quando um cliente usa credenciais padrão, Kerberos é o método de autenticação se a cadeia de conexão não for uma das seguintes: localhost, 127.0.0.1 ou \[ ::1 \] .

</dd> <dt>

**Estilo do controlador de teclado (KCS)**
</dt> <dd>

O protocolo usado pelo [*driver IPMI para*](windows-remote-management-glossary.md) se comunicar com o [*BMC (controlador de*](windows-remote-management-glossary.md)gerenciamento de placa base).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Um serviço de gerenciamento que implementa WS-Management protocolo para enviar e receber mensagens. O WinRM é um serviço de ouvinte. Um ouvinte é definido por um transporte (HTTP ou HTTPS) e um endereço IPv4 ou IPv6. Você pode criar mais de uma instância de ouvinte do WinRM em um único computador, dando a eles um endereço TCP/IP diferente ou número da porta.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**message**
</dt> <dd>

Um pacote de informações transmitidas entre computadores ou redes separadas construídas com o [*protocolo SOAP.*](windows-remote-management-glossary.md) O pacote tem um título que descreve o destino e o transporte da mensagem e um corpo que contém o conteúdo a ser usado quando a mensagem chega. Uma mensagem é uma combinação de elementos de especificações como [*WS-Addressing,*](windows-remote-management-glossary.md) [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management.*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Um [*namespace WMI,*](windows-remote-management-glossary.md) que é um grupo lógico de classes e instâncias WMI para controlar o escopo e o acesso. A fonte mais frequente de dados de gerenciamento para sistemas que executam Windows é o namespace cimv2 raiz, que contém classes como \\ [**o Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process). Os namespaces aparecem no URI do recurso para classes WMI, por https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service exemplo.

</dd> <dt>

**Negociar autenticação**
</dt> <dd>

Um tipo de autenticação negociado e de entrada único que é a Windows implementação do [*SPNEGO (Mecanismo*](windows-remote-management-glossary.md)de Negociação GSSAPI Simples e Protegido). A negociação de SPNEGO determina se a autenticação é tratada por Kerberos ou NTLM. Kerberos é o mecanismo preferencial. Negociar a autenticação Windows sistemas baseados em dados também é chamado Windows Autenticação Integrada.

</dd> <dt>

**sensor numérico**
</dt> <dd>

Um tipo numérico de sensor em um [*controlador de gerenciamento de placa base (BMC),*](windows-remote-management-glossary.md)por exemplo, temperatura ou tensão.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**opção**
</dt> <dd>

Os dados adicionais exigidos pelo provedor de recursos para processar uma solicitação. Por exemplo, alguns provedores WMI exigem dados adicionais fornecidos como [**objetos IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet.**](/windows/desktop/WmiSdk/swbemnamedvalueset) O suporte à opção é encontrado no [**objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**fora de banda**
</dt> <dd>

O aplicativo cliente obtém dados diretamente do [*BMC (controlador*](windows-remote-management-glossary.md) de gerenciamento de placa base) de outro computador, em vez de por meio do ouvinte [*WinRM*](windows-remote-management-glossary.md) no sistema operacional.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**Puxar**
</dt> <dd>

Uma [*mensagem de pull de enumeração WS*](windows-remote-management-glossary.md) é enviada para continuar uma enumeração iniciada por uma chamada inicial para WS-Enumeration:Enumerate. A operação de pull no serviço WinRM é executada por [**Enumerator.ReadItem**](enumerator-readitem.md) ou [**IWSManEnumerator::ReadItem.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**recurso**
</dt> <dd>

Um [*ponto de extremidade*](windows-remote-management-glossary.md) que representa um tipo distinto de operação de gerenciamento ou valor. Um serviço expõe um ou mais recursos e alguns recursos podem ter mais de uma instância. Um recurso de gerenciamento é semelhante a uma classe WMI ou uma tabela de banco de dados, e uma instância é semelhante a uma instância da classe ou uma linha na tabela. Por exemplo, a [**classe \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) representa um recurso. `Win32_LogicalDisk="C:\"` é uma instância específica do recurso.

</dd> <dt>

**URI do recurso**
</dt> <dd>

O [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) usado para identificar um tipo específico de recurso, como discos ou processos, em um sistema.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Sel**
</dt> <dd>

Consulte [*Log de Eventos do Sistema (SEL)*](windows-remote-management-glossary.md).

</dd> <dt>

**Adaptador SEL**
</dt> <dd>

O adaptador que envia [*dados do BMC (controlador de*](windows-remote-management-glossary.md) gerenciamento de placa base) para o Coletor de [*Eventos*](windows-remote-management-glossary.md).

</dd> <dt>

**Seletor**
</dt> <dd>

Um par nome e valor que representa uma instância específica de um [*recurso*](windows-remote-management-glossary.md). Isso é essencialmente um filtro ou uma "chave" que identifica a instância desejada do recurso. O suporte ao seletor é encontrado [**no objeto ResourceLocator.**](resourcelocator.md)

</dd> <dt>

**Sensor**
</dt> <dd>

Um dispositivo de medida em um [*BMC (controlador de*](windows-remote-management-glossary.md)gerenciamento de placa base).

</dd> <dt>

**service**
</dt> <dd>

Um aplicativo que fornece serviços de gerenciamento para clientes por meio do protocolo WS-Management e outros [*serviços Web.*](windows-remote-management-glossary.md) Um serviço geralmente é o mesmo que o [*ouvinte*](windows-remote-management-glossary.md) em uma rede. O serviço tem um endereço de transporte físico.

</dd> <dt>

**Sessão**
</dt> <dd>

Uma conexão entre um Windows de [*Gerenciamento*](windows-remote-management-glossary.md) Remoto e o ouvinte local ou remoto do [*WinRM*](windows-remote-management-glossary.md)ou serviço. Essa conexão é semelhante à conexão entre um script de cliente WMI e o WMI em um servidor remoto. As operações de sessão, como enumerar um recurso (Enumerar), obter uma instância de um recurso (Get) ou executar um método de recurso (Invoke) são métodos do **objeto Session.** Um **objeto** Session é criado [**por WSMan.CreateSession**](wsman-createsession.md).

</dd> <dt>

**SpNEGO (Mecanismo de Negociação GSS-API simples e protegido)**
</dt> <dd>

Um mecanismo de autenticação usado pelo cliente ou servidor que recebe solicitações de dados por meio do WinRM em um contexto do Active Directory. O SPNEGO é baseado em um protocolo RFC (Request For Comments) produzido pela IETF (Internet Engineering Task Force). SPNEGO também é conhecido como [*autenticação Windows*](windows-remote-management-glossary.md)integrado, o termo usado nos tópicos de ajuda Windows Gerenciamento Remoto.

</dd> <dt>

**SOAP (Protocolo Simples de Acesso a Objetos)**
</dt> <dd>

Um protocolo baseado em XML usado pelos serviços Web.

</dd> <dt>

**SOAP**
</dt> <dd>

Consulte [*Protocolo SOAP.*](windows-remote-management-glossary.md)

</dd> <dt>

**Spnego**
</dt> <dd>

Consulte [*SpNEGO (Mecanismo de Negociação GSS-API simples*](windows-remote-management-glossary.md)e protegido).

</dd> <dt>

**Log de Eventos do Sistema (SEL)**
</dt> <dd>

O banco de dados de eventos no hardware [*BMC (controlador*](windows-remote-management-glossary.md) de gerenciamento de placa base). O [*adaptador SEL*](windows-remote-management-glossary.md) transmite esses eventos para o sistema operacional.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**uniform resource identifier (URI)**
</dt> <dd>

Uma cadeia de caracteres que identifica um recurso na empresa, como um computador, um processo, uma unidade de disco ou um sensor de temperatura em um controlador de gerenciamento de [*placa base (BMC).*](windows-remote-management-glossary.md) O URI é o mecanismo de endereçamento de serviço Web definido na IETF (Internet Engineering Task Force) Uniform Resource Identifier (URI): Sintaxe genérica \[ RFC3986. \]

</dd> <dt>

**URI**
</dt> <dd>

Consulte [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**serviço Web**
</dt> <dd>

Um aplicativo de software usado para interação entre computadores pela Internet ou uma rede. Os serviços Web são descritos pela [*WSDL (Linguagem de*](windows-remote-management-glossary.md)Descrição do Serviço Web). A descrição específica do serviço Web informa a outros serviços como interagir com o serviço Web usando mensagens SOAP. As mensagens são transmitidas entre computadores por um transporte, normalmente HTTP ou HTTPS. [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md) são exemplos de protocolos usados por aplicativos de serviço Web para se comunicar entre si.

</dd> <dt>

**WSDL (Linguagem de Descrição do Serviço Web)**
</dt> <dd>

Uma linguagem baseada em XML usada para definir como interagir com um serviço Web. Normalmente, o WSDL descreve quais mensagens SOAP o serviço Web requer para retornar dados ou executar operações. O WSDL permite que uma implementação de um sistema operacional se comunique com o serviço Web implementado em outro sistema operacional, desde que os requisitos do WSDL sejam atendidos.

</dd> <dt>

**Autenticação Integrada do Windows**
</dt> <dd>

Consulte [*Negociar autenticação*](windows-remote-management-glossary.md).

</dd> <dt>

**WMI (Instrumentação de Gerenciamento do Windows)**
</dt> <dd>

A implementação da Microsoft do padrão WBEM (gerenciamento de Web-Based Enterprise) publicado pela [*DMTF (Distributed Management Task Force).*](windows-remote-management-glossary.md) O WMI permite que você gerencie computadores locais e remotos e modele objetos de computador e rede usando uma extensão [*do padrão CIM (modelo CIM).*](windows-remote-management-glossary.md)

</dd> <dt>

**Gerenciamento Remoto do Windows (WinRM)**
</dt> <dd>

A implementação da Microsoft de um serviço Web de gerenciamento com base no protocolo [*WS-Management*](windows-remote-management-glossary.md) padrão público.

</dd> <dt>

**Windows Shell Remoto (WinRS)**
</dt> <dd>

Uma ferramenta de shell que se baseia Windows [*Gerenciamento*](windows-remote-management-glossary.md) Remoto para executar comandos remotos, especialmente para servidores sem cabeça. A ferramenta de linha de comando é Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Consulte [*Windows WMI (Instrumentação de Gerenciamento de Dados).*](windows-remote-management-glossary.md)

</dd> <dt>

**Plug-in WMI**
</dt> <dd>

O plug-in WinRM que disponibiliza dados WMI para clientes WinRM.

</dd> <dt>

**WS-Addressing (wsa)**
</dt> <dd>

Um protocolo padrão público, baseado em SOAP, que cria um sistema de endereçamento usado nos headers de mensagens enviadas pela Internet. O padrão define como os recursos podem ser localizados em redes e firewalls. WS-Addressing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para enumerar uma sequência de elementos XML que pode representar coleções de dados, logs ou outras estruturas de informações lineares. WS-Enumeration é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, que permite que um serviço Web (o assinante) assine e aceite mensagens de notificação de eventos de outro serviço Web (a origem do evento). WS-Eventing é um dos protocolos de serviço Web que compõem o protocolo WS-Management.

</dd> <dt>

**WS-Management**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para compartilhar dados de gerenciamento entre todos os sistemas operacionais, computadores e dispositivos. Todas as [*mensagens*](windows-remote-management-glossary.md) enviadas pelo cliente ou pelos componentes do servidor WinRM usam esse protocolo.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Um protocolo padrão público, que é baseado em SOAP, para acessar representações XML de recursos baseados em serviços da Web por meio de um conjunto simples de verbos, como Get, put, Invoke ou Delete. WS-Transfer define as operações para enviar e receber a representação de um recurso específico e operações para criar ou excluir um recurso e sua representação correspondente.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Uma notação de caminho para endereçar partes de um documento XML, semelhante a uma URL. Uma expressão XPath é uma sequência de frases a serem obtidas do local atual no documento XML para outro nó ou conjunto de nós. As frases são separadas por caracteres de barra ("/"). O serviço WinRM dá suporte a [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) para [*dialeto de fragmento*](windows-remote-management-glossary.md).

</dd> </dl>

 

 