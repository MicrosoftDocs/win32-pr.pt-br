---
title: Funções de gerenciamento de perfil
description: Funções de gerenciamento de perfil
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Sistema de cores (WCS), funções
- WCS (Windows sistema de cores), funções
- gerenciamento de cores de imagem, funções
- gerenciamento de cores, funções
- cores, funções
- Referência do WCS, funções
- referência para WCS, funções
- Windows Sistema de cores (WCS), perfis
- WCS (Windows sistema de cores), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- Referência do WCS, perfis
- referência para WCS, perfis
- gerenciamento de perfil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f047c2dee199800fad976dd7b959fbbb54d585fd252fb8b5390c3223415db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587766"
---
# <a name="profile-management-functions"></a>Funções de gerenciamento de perfil

## <a name="profile-management-functions"></a>Funções de gerenciamento de perfil

As seguintes funções de API são úteis no gerenciamento de perfil.



| Função                                                                               | Descrição                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa um perfil de cor especificado a um dispositivo especificado.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte um [espaço de cor](c.md) lógico em um [perfil de dispositivo](d.md). |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desassocia um perfil de cor especificado a um dispositivo especificado em um computador especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos os perfis que atendem aos critérios de enumeração fornecidos. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | recupera o caminho do Windows diretório de cores em um computador especificado. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtém a rampa de gama de placas de exibição de cor direta.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera o perfil de cor registrado para o [espaço de cores](c.md)padrão especificado. |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala um determinado perfil para uso em um computador especificado. O perfil também é copiado para o diretório de cores. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa um valor de identificação especificado com a DLL do CMM (Dynamic Link Library) do módulo de gerenciamento de cores especificado. quando essa ID aparece em um perfil de cor, Windows pode localizar o CMM correspondente para criar uma transformação. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Define a rampa de gama em placas de exibição de cor direta.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra um perfil especificado para um espaço de [cores](c.md)padrão específico. O perfil pode ser consultado usando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Remove um perfil de cor especificado de um computador especificado. Os arquivos associados são excluídos opcionalmente do sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Dissocia um valor de ID especificado de uma determinada biblioteca de vínculo dinâmico (DLL do CMM) do módulo de gerenciamento de cores. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa um perfil de cor WCS especificado a um dispositivo especificado.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte um perfil WCS em um perfil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desassocia um perfil de cor WCS especificado com um dispositivo especificado em um computador especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos os perfis de cor que atendem aos critérios de enumeração no escopo de gerenciamento de perfil especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Retorna o tamanho, em bytes, do buffer exigido pela função [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar perfis de cor. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Recupera o perfil de cor padrão para um dispositivo ou o padrão independente do dispositivo, se o dispositivo não for especificado.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Retorna o tamanho, em bytes, do nome do perfil de cor padrão para um dispositivo, incluindo o terminador **nulo** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Recupera a tentativa de renderização padrão no escopo de gerenciamento de perfil especificado.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se o usuário optou por usar uma lista de associação de perfil por usuário para o dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Cria um identificador para um perfil de cor especificado.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Define o nome do perfil de cor padrão do tipo de perfil especificado no escopo de gerenciamento de perfil especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Define a tentativa de renderização padrão no escopo de gerenciamento de perfil especificado.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite que o usuário especifique se deseja usar uma lista de associação de perfil por usuário para o dispositivo especificado.                                              |



 

## <a name="profile-consumption-functions"></a>Funções de consumo de perfil

As APIs de consumo de perfil são aquelas em ICM2 que usam perfis de XML ICC ou WCS, identificadores de perfil ou tentativas de renderização como parâmetros e um conjunto de novas APIs para suporte de perfil WCS para o código de gerenciamento de cores do aplicativo.

 

## <a name="profiles-and-profile-management-functions"></a>Perfis e funções de gerenciamento de perfil

O fluxo de trabalho de gerenciamento de perfil é baseado em APIs ICM2 existentes que são aumentadas para fornecer funcionalidade adicional para a revisão do código do aplicativo.

Os perfis contêm informações usadas por algoritmos de processamento de cores para converter a cor entre espaços de cores diferentes. O gerenciamento de perfil fornece uma maneira de consultar e especificar quais perfis são usados em diferentes estágios pelo modelo de processamento de cores para gerenciar a saída de cores de vários dispositivos periféricos com características de cores diversas.

O gerenciamento de perfil fornece o seguinte conjunto de funcionalidades:

 

1. Instalando perfis de cor para uso no sistema.

 

2. Associação de um ou mais perfis de cor instalados a qualquer dispositivo específico.

 

3. Escolher um perfil de cor padrão de um tipo específico entre os perfis disponíveis para uso em um estágio específico de processamento de cores. Isso pode ser para um dispositivo entre os perfis associados a ele, ou entre os perfis instalados no sistema e não específico ao dispositivo.

 

4. Enumerar perfis de cor que satisfaçam critérios específicos entre os perfis instalados no sistema.

As extensões de nome de arquivo do perfil WCS são ". CDMP" para DMPs, ". Camp" para acampamentos e ". gmmp" para GMMPs.

 

**Gerenciamento de perfil por usuário e habilitação da execução no contexto LUA**

A meta do design descrito no documento atual é a seguinte:

 

1. A implementação de ICM2 herdada não oferece suporte para o gerenciamento de perfil por usuário. Usuários diferentes não podem ter suas próprias configurações de perfil. No Vista, a infraestrutura de gerenciamento do perfil WCS permite que os usuários definam configurações de perfil individuais para a maioria das funcionalidades.

 

2. Todas as APIs de gerenciamento de perfil ICM2 herdadas modificam configurações de todo o sistema e exigem privilégios administrativos. no Windows Vista, todos os usuários são executados em configurações de LUA (conta de usuário com privilégios mínimos) na maioria das vezes, e os administradores podem elevar o privilégio de forma seletiva para executar aplicativos que modificam as configurações de todo o sistema. No gerenciamento de perfil WCS, todas as configurações de perfil por usuário são configuráveis no contexto LUA. Os aplicativos de gerenciamento de perfil podem ser executados como configurações de LUA, aumentando seu escopo de uso e garantindo que a segurança do sistema não seja comprometida.

O gerenciamento de perfil no Vista fornece os seguintes aprimoramentos em relação à infraestrutura de ICM2 herdada:

 

1. Ele habilita a associação de perfil com dispositivos, configurações de perfil padrão e enumeração de perfis no escopo de todo o usuário e do sistema.

 

2. A instalação de um perfil permanece em todo o sistema e requer privilégios de administrador. Isso é consistente com a instalação do perfil durante a instalação do dispositivo porque a instalação do dispositivo é de todo o sistema e requer privilégios administrativos.

 

Se os dispositivos podem ser instalados do contexto LUA é específico ao que tem suporte para essa classe de dispositivo. Por exemplo, no Vista, é possível fazer a instalação da impressora do contexto LUA se o usuário tiver concedido direitos para copiar arquivos no repositório de drivers por um administrador de domínio usando políticas de repositório de driver. A infraestrutura de gerenciamento do perfil de cores não precisa fazer nada de especial nesse sentido, já que a instalação ocorre no contexto do spooler.

 

3. A modificação das configurações de perfil no escopo por usuário pode ser feita no contexto LUA; modificações em todo o sistema exigem privilégios administrativos. As operações de gerenciamento de perfil que exigem a leitura de informações de configuração podem ser feitas no contexto de LUA para as configurações por usuário e para todo o sistema.

Escopo de gerenciamento de perfil indica o escopo das operações executadas; por usuário ou por todo o sistema.

Para cada operação, é indicado se pode ser feito a partir do contexto LUA. Se uma operação não puder ser executada no contexto LUA, a API de gerenciamento de perfil correspondente retornará uma falha com acesso negado. Os aplicativos que usam a API, como o painel de controle de gerenciamento de cores, podem permitir que o usuário eleve o contexto administrativo (usando OTS ou a interface do usuário de consentimento) e, em seguida, chame a API do contexto elevado para que a operação seja realizada com sucesso.



Operação

Escopo de gerenciamento de perfil

Pré-condição

Pós-condição

Executável no contexto LUA

$ {ROWSPAN2} $Install do perfil $ {remover} $  

Todo o sistema

Perfil copiado, instalado no sistema e disponível para uso. O perfil é enumerável em todo o sistema e no escopo do usuário atual para todos os usuários.

Durante a instalação do driver de dispositivo, governada pelas políticas de instalação do driver. No, otherwise.

Usuário atual

Sem suporte

$ {ROWSPAN2} $Uninstall do perfil $ {remover} $  

Todo o sistema

O perfil está instalado no sistema

Perfil desinstalado do sistema e, opcionalmente, excluído do repositório de perfis. O perfil não está mais disponível para uso e não é enumerável em nenhum escopo.

Não

Usuário atual

Sem suporte

$ {ROWSPAN2} $Associate o perfil com o dispositivo $ {REMOVE} $  

Todo o sistema

O perfil está instalado e é do tipo ICC ou CDMP

O perfil está disponível para uso com o dispositivo por todos os usuários. Ele é enumerável, no escopo de todo o sistema e também no escopo do usuário atual para todos os usuários, como associado ao dispositivo.

Não

Usuário atual

O perfil está instalado. Não importa se o perfil já está associado ao dispositivo no escopo de todo o sistema e é do tipo ICC ou CDMP.

O perfil está disponível para uso com o dispositivo pelo usuário atual. Ele é enumerável somente no escopo do usuário atual (a menos que também haja uma associação em todo o sistema) como associado ao dispositivo.

Sim

$ {ROWSPAN2} $Disassociate o perfil do dispositivo $ {REMOVE} $  

Todo o sistema

O perfil está associado ao dispositivo no escopo de todo o sistema e é do tipo ICC ou CDMP

O perfil não está mais disponível para uso (exceto para usuários que têm essa associação em seu escopo de usuário atual também). Não é enumerável no escopo de todo o sistema. No entanto, pode ser enumerável no escopo do usuário atual, para um usuário que tenha essa associação em seu escopo.

Não

Usuário atual

O perfil está associado ao dispositivo no escopo do usuário atual (independentemente de estar associado no escopo de todo o sistema) e é do tipo ICC ou CDMP.

O perfil não está mais disponível para uso ou enumerável como associado ao dispositivo, pelo usuário atual (a menos que ele também esteja associado no escopo de todo o sistema ao dispositivo).

Sim

$ {ROWSPAN2} $Set o perfil para um tipo (DMP ou ICC) como padrão para um dispositivo $ {REMOVE} $  

Todo o sistema

O perfil é do tipo ICC ou CDMP

O perfil é usado por padrão para o tipo específico com o dispositivo, para todos os usuários, exceto aqueles que substituíram essa configuração em seu escopo de usuário atual. (O perfil é instalado e associado ao sistema de dispositivos em todo, se esse ainda não for o caso.)

Não

Usuário atual

O perfil é do tipo ICC ou CDMP

O perfil é usado por padrão para o tipo específico com o dispositivo no caso do usuário atual, independentemente do padrão de todo o sistema para isso. (O perfil é instalado e associado ao dispositivo para o usuário atual, se esse ainda não for o caso.)

Sim, se o perfil já estiver instalado

$ {ROWSPAN2} $Set o perfil para um tipo (ICC, DMP, CAMP, GMMP) e a combinação de subtipo como padrão global $ {REMOVE} $  

Todo o sistema

Somente perfis ICC e CDMP podem ser associados a dispositivos.

O perfil é usado por padrão para o tipo específico. Os usuários podem substituir essa configuração no escopo do usuário atual. (O perfil é instalado, se esse ainda não for o caso.)

Não

Usuário atual

Somente perfis ICC e CDMP podem ser associados a dispositivos.

O perfil é usado por padrão para o tipo específico para o usuário atual. (O perfil é instalado, se esse ainda não for o caso.)

Sim, se o perfil já estiver instalado.

$ {ROWSPAN2} $Erase a substituição do usuário atual para uma configuração de perfil padrão específica, para que o padrão do sistema sempre seja usado (como fallback) mesmo para o escopo do usuário atual. $ {REMOVE} $  

Todo o sistema

Não se aplica

Usuário atual

Mesmo para consultas de usuário atual em configurações de perfil padrão, as configurações de todo o sistema são retornadas para uso.

Sim

$ {ROWSPAN2} $Enumerate perfis instalados que atendem a critérios específicos (como classe de dispositivo, classe de perfil, etc.) $ {REMOVER} $  

Todo o sistema

Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.

Os perfis que estão instalados e atendem aos critérios especificados no escopo de todo o sistema são enumerados.

Sim

Usuário atual

Somente perfis ICC e CDMP podem ser associados a dispositivos e, portanto, enumerados para dispositivos.

Os perfis que estão instalados e atendem aos critérios especificados no escopo de todo o sistema são enumerados.

Sim

$ {ROWSPAN2} $Enumerate perfis associados a um dispositivo específico que atendem a critérios específicos, como classe de dispositivo e classe de perfil $ {REMOVE} $  

Todo o sistema

Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.

Os perfis associados ao dispositivo no escopo de todo o sistema e atendem aos critérios especificados no escopo de todo o sistema são enumerados.

Sim

Usuário atual

Somente perfis ICC e CDMP podem ser associados e enumerados para dispositivos.

Os perfis que estão disponíveis como associados ao dispositivo no escopo do usuário atual, que inclui as associações de todo o sistema e atendem aos critérios especificados no escopo do usuário atual são enumerados.

Sim



 

Os tipos de perfil de cor válidos são fornecidos pela enumeração COLORPROFILETYPE.

Os subtipos de perfil de cor válidos são fornecidos pela enumeração COLORPROFILESUBTYPE.

As combinações de tipo/subtipo de perfil válidas são mostradas na tabela a seguir.



COLORPROFILETYPE 

COLORPROFILESUBTYPE válido

Observações

Padrão do dispositivo

Padrão global

Uso pretendido

Uso pretendido

\_ICC CPT

CPST \_ nenhum

Obter/definir perfil ICC padrão associado a um dispositivo

CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace

Obter/definir perfil ICC como global RGB ou perfil de espaço de trabalho personalizado. Consulte a observação.

O COLORPROFILETYPE CPT \_ ICC e o CPT \_ DMP são mutuamente exclusivos. O perfil de cor padrão definido para um determinado espaço de trabalho (RGB ou personalizado) pode ser um perfil ICC ou um perfil DMP, mas não ambos.

CPT \_ DMP

CPST \_ nenhum

Obter/definir perfil DMP padrão associado a um dispositivo

CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace

Obter/definir perfil DMP como global RGB ou perfil de espaço de trabalho personalizado. Consulte a observação.

O COLORPROFILETYPE CPT \_ ICC e o CPT \_ DMP são mutuamente exclusivos. O perfil de cor padrão definido para um determinado espaço de trabalho (RGB ou personalizado) pode ser um perfil ICC ou um perfil DMP, mas não ambos.



 

> [!Note]  
> Quando WcsSetDefaultColorProfile é chamado para definir um perfil DMP como o perfil padrão para o espaço de trabalho RGB ou um espaço de trabalho personalizado, somente um perfil DMP que é do tipo RGBVirtualDevice, LCD ou CRT é válido.
>
>  
>
> Quando WcsSetDefaultColorProfile é chamado para definir um perfil ICC como o perfil padrão para o espaço de trabalho RGB ou um espaço de trabalho personalizado, somente um perfil ICC cuja classe é "spac" ou "Disp" e cujo espaço de cores é "RGB" é válido.

 

A arquitetura é projetada de acordo com os requisitos das operações, conforme mencionado nas enumerações e tabelas acima.

### <a name="profile-management-public-api-layer"></a>Camada de API pública de gerenciamento de perfil

Como o escopo de gerenciamento de perfil não é suportado por APIs ICM2 herdadas, um novo conjunto de APIs de gerenciamento de perfil WCS é necessário que define o escopo de gerenciamento de perfil como usuário de todo o sistema ou atual. ? As APIs de ICM2 herdadas continuam com suporte para compatibilidade com versões anteriores e funcionam no escopo de gerenciamento de perfil que é implícito para a chamada. o ICM2 APIs que funcionam no escopo do usuário atual? Isso é para operações que têm suporte para o escopo do usuário em todo e no momento no gerenciamento do perfil do WCS. As APIs herdadas do ICM2 chamam novas APIs do WCS com o escopo de gerenciamento de perfis como usuário atual. Isso faz sentido da perspectiva do usuário porque isso permite configurações por usuário de aplicativos herdados e também a execução da maioria das operações no contexto de LUA. o ICM2 APIs que funcionam no escopo de todo o sistema? Isso é para operações (perfis de instalação e perfis de desinstalação) que dão suporte apenas ao escopo de todo o sistema. Nenhuma nova API de gerenciamento de perfil WCS é criada e APIs existentes podem ser modificadas.

As implementações subjacentes das operações de gerenciamento de perfil funcionam nas seguintes entidades de dados de configuração para criar o contexto para algoritmos de processamento de cores para fornecer funcionalidades de gerenciamento de cores. Eles são configurações específicas de dispositivo ou globais (independentes de dispositivo). dados de configuração específicos do dispositivo:? Lista de perfis associados a um dispositivo específico. ? Perfil padrão para tipos de perfil diferentes associados a um dispositivo. ? Modo de correspondência de perfis usados para enumeração. o dados de configuração global:? Lista de perfis instalados no sistema. ? Perfil padrão global para tipos de perfil diferentes. ? As implementações subjacentes do armazenamento de dados de configuração assumem o escopo de armazenamento para dados de configuração (dispositivo independente ou específico de dispositivo), que pode ser o usuário de todo o sistema ou o atual. Isso é diferente do escopo de gerenciamento de perfil. Uma operação com o escopo de gerenciamento de perfil de usuário atual pode causar uma leitura de um escopo de armazenamento em todo o sistema se a configuração de usuário atual para essa operação não estiver presente. ? A camada de API ICM2/WCS chama essa camada de armazenamento para obter e definir dados com o escopo de armazenamento apropriado. A camada de armazenamento é transparente para o escopo de gerenciamento de perfil. A lógica para combinar dados de escopos de armazenamento de usuário atual e de todo o sistema para criar ou atualizar uma configuração de acordo com o escopo de gerenciamento de perfil especificado pelo chamador da API. Essa lógica está presente na camada de API ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Camada de armazenamento específica do dispositivo

O armazenamento para diferentes classes de dispositivos, como impressão, captura ou exibição, pode ser diferente entre si. Por exemplo, os dados de configuração para um dispositivo de impressão devem ser armazenados usando APIs de impressão padrão, como SetPrinterDataEx e GetPrinterDataEx, para permitir que os perfis sejam copiados e as configurações sejam transferidas para um computador cliente durante a conexão de apontar e imprimir. ? Essa camada exporta a funcionalidade para abrir armazenamento, obter dados, definir dados e fechar a loja usando interfaces predefinidas comuns para que a camada de armazenamento de configuração de gerenciamento de perfil possa chamá-las enquanto são transparentes para o modo como os dados são armazenados para esse dispositivo.

O diagrama a seguir ilustra essa arquitetura.



Camada de API pública de gerenciamento de perfil

$ {ROWSPAN2} $Legacy APIs ICM2 para operações que dão suporte apenas ao escopo de gerenciamento de perfil em todo o sistema no Vista (instalar, desinstalar e obter o diretório de cores). Eles chamam a camada de armazenamento de configuração com o escopo de armazenamento apropriado. $ {REMOVE} $  

API ICM2 herdada para operações que dão suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema no Vista (todas as operações diferentes de instalar, desinstalar e obter o diretório de cores). Eles trabalham implicitamente no escopo do usuário atual e chamam a nova API do WCS com o escopo de gerenciamento de perfil como usuário atual.

Nova API WCS com suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema. Eles chamam a camada de armazenamento de configuração com o escopo de armazenamento apropriado.



 



configuração de gerenciamento de perfil Armazenamento camada

Rotinas de configuração global independentes de dispositivo

Rotinas de configuração específicas do dispositivo

$ {ROWSPAN3} $Profile a instalação e o gerenciamento de configurações de perfil padrão independente de dispositivo, com suporte no escopo de armazenamento de todo o sistema e do usuário atual. $ {REMOVE} $  

Associação de dispositivo e gerenciamento de configurações de perfil padrão específicas do dispositivo, com suporte no escopo de armazenamento de todo o sistema e do usuário atual.

Device-Specific Armazenamento camada

Imprimir armazenamento específico

Exibir armazenamento específico

Capturar armazenamento específico



 

APIs ICM2 herdadas para operações que dão suporte apenas ao escopo de gerenciamento de perfil em todo o sistema no Vista não têm alterações no comportamento. As operações de instalação e desinstalação caem nesta categoria.

APIs ICM2 herdadas para operações que dão suporte a escopo de gerenciamento de perfil de usuário atual e de todo o sistema têm seu comportamento alterado para consultar e definir as configurações do usuário atual. Todas as operações que não sejam instalar e desinstalar se enquadram nesta categoria.

 

 




