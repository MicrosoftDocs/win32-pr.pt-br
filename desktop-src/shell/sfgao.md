---
description: Atributos que podem ser recuperados em um item (arquivo ou pasta) ou conjunto de itens.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ae5dca355b7c22e3075a0ced7640a5bd45a54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481982"
---
# <a name="sfgao"></a>SFGAO

Atributos que podem ser recuperados em um item (arquivo ou pasta) ou conjunto de itens.




| Constante/valor | Descrição | 
|----------------|-------------|
| <span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl><dt><strong>SFGAO_CANCOPY</strong></dt><dt>0x00000001</dt></dl> | Os itens especificados podem ser copiados.<br /> | 
| <span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl><dt><strong>SFGAO_CANMOVE</strong></dt><dt>0x00000002</dt></dl> | Os itens especificados podem ser movidos.<br /> | 
| <span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl><dt><strong>SFGAO_CANLINK</strong></dt><dt>0x00000004</dt></dl> | Atalhos podem ser criados para os itens especificados. Esse atributo tem o mesmo valor que <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br /> Se uma extensão de namespace <strong></strong> retornar esse atributo, uma entrada Criar Atalho com um manipulador padrão será adicionada ao menu de atalho exibido durante operações do tipo "arrastar e soltar". A extensão também pode implementar seu próprio manipulador para o <em>verbo de link</em> no lugar do padrão. Se a extensão fizer isso, ela será responsável por criar o atalho.<br /> Um <strong>item Criar Atalho</strong> também é adicionado ao menu arquivo Windows Explorer <strong>e</strong> aos menus de atalho normais.<br /> Se o item estiver selecionado, o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> do aplicativo será invocado com o membro <strong>lpVerb</strong> da estrutura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> definida para <em>vincular</em>. Seu aplicativo é responsável por criar o link.<br /> | 
| <span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl><dt><strong>SFGAO_STORAGE</strong></dt><dt>0x00000008</dt></dl> | Os itens especificados podem ser vinculados a <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>um objeto IStorage</strong></a> por <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>meio de IShellFolder::BindToObject.</strong></a> Para obter mais informações sobre os recursos de manipulação de namespace, consulte <strong>IStorage</strong>.<br /> | 
| <span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl><dt><strong>SFGAO_CANRENAME</strong></dt><dt>0x00000010</dt></dl> | Os itens especificados podem ser renomeados. Observe que esse valor é essencialmente uma sugestão; nem todos os clientes de namespace permitem que os itens sejam renomeados. No entanto, aqueles que têm devem ter esse atributo definido.<br /> | 
| <span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl><dt><strong>SFGAO_CANDELETE</strong></dt><dt>0x00000020</dt></dl> | Os itens especificados podem ser excluídos.<br /> | 
| <span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl><dt><strong>SFGAO_HASPROPSHEET</strong></dt><dt>0x00000040</dt></dl> | Os itens especificados têm folhas de propriedades.<br /> | 
| <span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl><dt><strong>SFGAO_DROPTARGET</strong></dt><dt>0x00000100</dt></dl> | Os itens especificados são destinos de soltar.<br /> | 
| <span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl><dt><strong>SFGAO_CAPABILITYMASK</strong></dt><dt>0x00000177</dt></dl> | Esse sinalizador é uma máscara para os atributos de funcionalidade: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET e SFGAO_DROPTARGET. Normalmente, os chamadores não usam esse valor.<br /> | 
| <span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl><dt><strong>SFGAO_SYSTEM</strong></dt><dt>0x00001000</dt></dl> | <strong>Windows 7 e posterior.</strong> Os itens especificados são itens do sistema.<br /> | 
| <span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl><dt><strong>SFGAO_ENCRYPTED</strong></dt><dt>0x00002000</dt></dl> | Os itens especificados são criptografados e podem exigir apresentação especial.<br /> | 
| <span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl><dt><strong>SFGAO_ISSLOW</strong></dt><dt>0x00004000</dt></dl> | O acesso ao item (por <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>meio de IStream</strong></a> ou outras interfaces de armazenamento) deve ser uma operação lenta. Os aplicativos devem evitar o acesso a itens sinalizados com SFGAO_ISSLOW. <br /><blockquote>[!Note]<br />Abrir um fluxo para um item geralmente é uma operação lenta em todos os momentos. SFGAO_ISSLOW indica que ele deve ser especialmente lento, por exemplo, no caso de conexões de rede lentas ou arquivos offline (FILE_ATTRIBUTE_OFFLINE). No entanto, a consulta SFGAO_ISSLOW é uma operação lenta. Os aplicativos devem consultar SFGAO_ISSLOW somente em um thread em segundo plano. Um método alternativo, como a recuperação da propriedade <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> e o teste para FILE_ATTRIBUTE_OFFLINE, pode ser usado no lugar de uma chamada de método que envolve SFGAO_ISSLOW.</blockquote><br /> | 
| <span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl><dt><strong>SFGAO_GHOSTED</strong></dt><dt>0x00008000</dt></dl> | Os itens especificados são mostrados como esmaecidas e não estão disponíveis para o usuário.<br /> | 
| <span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl><dt><strong>SFGAO_LINK</strong></dt><dt>0x00010000</dt></dl> | Os itens especificados são atalhos.<br /> | 
| <span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl><dt><strong>SFGAO_SHARE</strong></dt><dt>0x00020000</dt></dl> | Os objetos especificados são compartilhados.<br /> | 
| <span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl><dt><strong>SFGAO_READONLY</strong></dt><dt>0x00040000</dt></dl> | Os itens especificados são somente leitura. No caso de pastas, isso significa que novos itens não podem ser criados nessas pastas. Isso não deve ser confundido com o comportamento especificado pelo sinalizador FILE_ATTRIBUTE_READONLY recuperado por <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> em uma estrutura <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA.</strong></a> FILE_ATTRIBUTE_READONLY tem nenhum significado para pastas do sistema de arquivos Win32.<br /> | 
| <span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl><dt><strong>SFGAO_HIDDEN</strong></dt><dt>0x00080000</dt></dl> | O item está oculto e não deve ser exibido, a menos que a opção Mostrar arquivos e pastas <strong>ocultas</strong> esteja habilitada em <strong>Pasta Configurações</strong>.<br /> | 
| <span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl><dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt><dt>0x000FC000</dt></dl> | Não use.<br /> | 
| <span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl><dt><strong>SFGAO_NONENUMERATED</strong></dt><dt>0x00100000</dt></dl> | Os itens são itens não numerados e devem estar ocultos. Eles não são retornados por meio de um enumerador como o criado pelo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>método IShellFolder::EnumObjects.</strong></a><br /> | 
| <span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl><dt><strong>SFGAO_NEWCONTENT</strong></dt><dt>0x00200000</dt></dl> | Os itens contêm novo conteúdo, conforme definido pelo aplicativo específico.<br /> | 
| <span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl><dt><strong>SFGAO_CANMONIKER</strong></dt></dl> | Sem suporte.<br /> | 
| <span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl><dt><strong>SFGAO_HASSTORAGE</strong></dt></dl> | Sem suporte.<br /> | 
| <span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl><dt><strong>SFGAO_STREAM</strong></dt><dt>0x00400000</dt></dl> | Indica que o item tem um fluxo associado a ele. Esse fluxo pode ser acessado por meio de uma chamada para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a> com IID_IStream no <em>parâmetro riid.</em><br /> | 
| <span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl><dt><strong>SFGAO_STORAGEANCESTOR</strong></dt><dt>0x00800000</dt></dl> | Os filhos desse item podem ser acessados <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>por meio de IStream</strong></a> <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>ou IStorage.</strong></a> Esses filhos são sinalizados com SFGAO_STORAGE ou SFGAO_STREAM.<br /> | 
| <span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl><dt><strong>SFGAO_VALIDATE</strong></dt><dt>0x01000000</dt></dl> | Quando especificado como entrada, SFGAO_VALIDATE instrui a pasta a validar se os itens contidos em uma pasta ou matriz de itens do Shell existem. Se um ou mais desses itens não existirem, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder::GetAttributesOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellItemArray::GetAttributes</strong></a> retornarão um código de falha. Esse sinalizador nunca é retornado como um valor [out].<br /> Quando usado com a pasta do sistema de arquivos, o SFGAO_VALIDATE instrui a pasta a descartar propriedades armazenadas em cache recuperadas por clientes de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2::GetDetailsEx</strong></a> que podem ter se acumulado para os itens especificados.<br /> | 
| <span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl><dt><strong>SFGAO_REMOVABLE</strong></dt><dt>0x02000000</dt></dl> | Os itens especificados estão em mídia removível ou são dispositivos removíveis.<br /> | 
| <span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl><dt><strong>SFGAO_COMPRESSED</strong></dt><dt>0x04000000</dt></dl> | Os itens especificados são compactados.<br /> | 
| <span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl><dt><strong>SFGAO_BROWSABLE</strong></dt><dt>0x08000000</dt></dl> | Os itens especificados podem ser hospedados dentro de um navegador da Web ou Windows do Explorer.<br /> | 
| <span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl><dt><strong>SFGAO_FILESYSANCESTOR</strong></dt><dt>0x10000000</dt></dl> | As pastas especificadas são pastas do sistema de arquivos ou contêm pelo menos um descendente (filho, descendente ou posterior) que é uma pasta do sistema de arquivos (SFGAO_FILESYSTEM).<br /> | 
| <span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl><dt><strong>SFGAO_FOLDER</strong></dt><dt>0x20000000</dt></dl> | Os itens especificados são pastas. Alguns itens podem ser sinalizados com SFGAO_STREAM e SFGAO_FOLDER, como um arquivo compactado com uma extensão .zip nome de arquivo. Alguns aplicativos podem incluir esse sinalizador ao testar itens que são arquivos e contêineres.<br /> | 
| <span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl><dt><strong>SFGAO_FILESYSTEM</strong></dt><dt>0x40000000</dt></dl> | As pastas ou arquivos especificados fazem parte do sistema de arquivos (ou seja, são arquivos, diretórios ou diretórios raiz). Os nomes analisados dos itens podem ser presumidos como caminhos válidos do sistema de arquivos Win32. Esses caminhos podem ser UNC ou baseados em letra da unidade.<br /> | 
| <span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl><dt><strong>SFGAO_STORAGECAPMASK</strong></dt><dt>0x70C50008</dt></dl> | Esse sinalizador é uma máscara para os atributos de funcionalidade de armazenamento: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER e SFGAO_FILESYSTEM. Os chamadores normalmente não usam esse valor.<br /> | 
| <span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl><dt><strong>SFGAO_HASSUBFOLDER</strong></dt><dt>0x80000000</dt></dl> | As pastas especificadas têm subpastas. O atributo SFGAO_HASSUBFOLDER é apenas consultoria e pode ser retornado por implementações de pastas do Shell, mesmo que eles não contenham subpastas. Observe, no entanto, que o inverso — falha ao retornar SFGAO_HASSUBFOLDER — afirma definiamente que os objetos de pasta não têm subpastas.<br /> O retorno de SFGAO_HASSUBFOLDER é recomendado sempre que uma quantidade significativa de tempo é necessária para determinar se existem subpastas. Por exemplo, o shell sempre retorna SFGAO_HASSUBFOLDER quando uma pasta está localizada em uma unidade de rede.<br /> | 
| <span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl><dt><strong>SFGAO_CONTENTSMASK</strong></dt><dt>0x80000000</dt></dl> | Este sinalizador é uma máscara para atributos de conteúdo, no momento, somente SFGAO_HASSUBFOLDER. Os chamadores normalmente não usam esse valor.<br /> | 
| <span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl><dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt><dt>0x81044000</dt></dl> | Máscara usada pela propriedade <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> para determinar atributos que são considerados para causar cálculos lentos ou ausência de contexto: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER e SFGAO_VALIDATE. Os chamadores normalmente não usam esse valor.<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray:: GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
