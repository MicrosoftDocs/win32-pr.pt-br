---
title: Chaves do Registro COM
description: Chaves do Registro COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80800bda0123823fec85a514c19031d485b17baca729969b4e74e5f08516eecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048493"
---
# <a name="com-registry-keys"></a>Chaves do Registro COM

O registro contém uma grande quantidade de informações usadas pelo COM. As informações mais importantes são armazenadas nas chaves a seguir.



| Chave                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Grupos de opções de configuração (um conjunto de valores nomeados) para um ou mais objetos COM distribuídos em um local no Registro. As sub-chaves nessa chave são usadas para mapear um AppID (identificador de aplicativo) para um nome de servidor remoto. Para simplificar o gerenciamento de definições comuns de configuração e segurança, os objetos COM distribuídos hospedados pelo mesmo executável são agrupados em uma AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [Clsid](clsid-key-hklm.md)<br/>                              | Um CLSID (identificador de classe) é um identificador global exclusivo que identifica um objeto de classe COM. Se o servidor ou contêiner permitir a vinculação a objetos inseridos, registre um CLSID para cada classe de objetos com suporte. A chave CLSID contém informações usadas pelo manipulador COM padrão para retornar informações sobre uma classe quando ela está no estado de execução.<br/> Para obter um CLSID para seu aplicativo, use uuidgen.exe, encontrado no diretório \\ TOOLs do com Toolkit ou use [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Um ProgID (identificador programático) é uma entrada do Registro que pode ser associada a um CLSID. A chave ProgID mapeia uma cadeia de caracteres amigável para um CLSID. Como o CLSID, o ProgID identifica uma classe, mas com menos precisão. Use um ProgID em situações de programação em que não é possível usar um CLSID. ProgIDs não devem aparecer na interface do usuário. Não há garantia de que os ProgIDs sejam exclusivos, portanto, eles só podem ser usados quando colisões de nome não ocorrerem.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Associa um ProgID a um CLSID. Ele é usado para determinar a versão mais recente de um aplicativo de objeto. Assim como o ProgID, o ProgID independente de versão pode ser registrado com um nome acessível por humanos. <br/> Os aplicativos devem registrar um identificador programático independente de versão na chave VersionIndependentProgID. O ProgID independente de versão refere-se à classe do aplicativo e não muda de versão para versão, permanecendo constante em todas as versões. Ele é usado com linguagens de macro e refere-se à versão instalada no momento da classe do aplicativo. O ProgID independente de versão deve corresponder ao nome da versão mais recente do aplicativo de objeto. <br/> |
| [extensão de \_ arquivo](-file-extension--key.md)<br/>              | Associa uma extensão de nome de arquivo a um ProgID.<br/> As informações contidas na chave de extensão de nome de arquivo são usadas pelos [monikers](file-monikers.md)do sistema e do arquivo . [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa a chave de extensão de nome de arquivo para fornecer o CLSID associado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interface](interface-key.md)<br/>                           | Registra novas interfaces associando um nome de interface a um IID (identificador de interface). Ele mapeia IIDs para informações específicas para uma interface. As informações são necessárias principalmente para usar interfaces entre limites de processo. <br/> Ao adicionar uma nova interface, a tecla Interface deve ser concluída para COM registrar a nova interface. Deve haver uma sub-chave IID para cada nova interface. <br/>                                                                                                                                                                                                                                                                                                       |
| [Ole](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controla as permissões de início e acesso padrão para objetos COM distribuídos, bem como recursos de segurança de nível de chamada para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Somente os administradores têm acesso completo a essa parte do Registro. Todos os outros usuários têm acesso somente leitura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 





